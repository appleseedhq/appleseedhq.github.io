---
title: Download Statistics
area: stats
layout: default
section: stats
---

## Download Statistics

<div id="download-stats">Retrieving Statistics...</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/handlebars.js/2.0.0/handlebars.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.9.0/moment.min.js"></script>

{% raw %}
<script id="render-download-stats-template" type="text/x-handlebars-template">
    {{#each this}}
        <div class="release">
            <h3>
                <a href="{{ html_url }}">{{ name }}</a>
            </h3>
            <p>Released on {{ created_at }} ({{ created_ago }})</p>
            <table>
                <thead>
                    <tr>
                        <th class="file">File</th>
                        <th class="count">Downloads</th>
                    </tr>
                </thead>
                <tbody>
                    {{#each assets}}
                        <tr>
                            <td class="file">
                                <a href="{{ browser_download_url }}">{{ name }}</a>
                            </td>
                            <td class="count">{{ download_count }}</td>
                        </tr>
                    {{/each}}
                </tbody>
                <tfoot>
                    <tr>
                        <td class="file">Total</td>
                        <td class="count">{{ total_downloads }}</td>
                    </tr>
                </tfoot>
            </table>
        </div>
    {{/each}}
</script>
{% endraw %}

<script type="text/javascript">
    $(document).ready(function () {
        var renderDownloadStatsSrc = $("#render-download-stats-template").html();
        var renderDownloadStats = Handlebars.compile(renderDownloadStatsSrc);

        var processReleases = function (releases) {
            releases = releases.sort(function (lhs, rhs) {
                var lhsDate = Date.parse(lhs.created_at);
                var rhsDate = Date.parse(rhs.created_at);
                return lhsDate < rhsDate ? +1 :
                       lhsDate > rhsDate ? -1 : 0;
            });

            releases.forEach(function (release) {
                release.assets = release.assets.sort(function (lhs, rhs) {
                    var lhsCount = lhs.download_count;
                    var rhsCount = rhs.download_count;
                    return lhsCount < rhsCount ? +1 :
                           lhsCount > rhsCount ? -1 : 0;
                });

                release.total_downloads = 0;
                release.assets.forEach(function (asset) {
                    release.total_downloads += asset.download_count;
                });

                var createdAt = moment(release.created_at);
                release.created_at = createdAt.format('MMMM Do YYYY, h:mm:ss a');
                release.created_ago = createdAt.fromNow();
            });

            var html = renderDownloadStats(releases);
            $("#download-stats").replaceWith(html);
        };

        if (true) {
            $.getJSON("https://api.github.com/repos/appleseedhq/appleseed/releases", function (appleseedReleases) {
                $.getJSON("https://api.github.com/repos/appleseedhq/appleseed-scenes/releases", function (scenesReleases) {
                    var releases = appleseedReleases.concat(scenesReleases);
                    processReleases(releases);
                });
            });
        } else {
            processReleases({% include releases.json %});
        }
    });
</script>
