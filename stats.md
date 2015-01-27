---
title: Download Statistics
layout: default
section: stats
---

## Download Statistics

<div id="download-stats">Retrieving Statistics...</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/handlebars.js/2.0.0/handlebars.min.js"></script>

{% raw %}
<script id="render-download-stats-template" type="text/x-handlebars-template">
    {{#each this}}
        <div class="release">
            <h3>{{ name }}</h3>
            <p>Creation Date: {{ created_at }}</p>
            <table>
                <tr>
                    <th class="name">File</th>
                    <th class="value">Downloads</th>
                </tr>
                {{#each assets}}
                    <tr>
                        <td class="name">{{ name }}</td>
                        <td class="value">{{ download_count }}</td>
                    </tr>
                {{/each}}
            </table>
        </div>
    {{/each}}
</script>
{% endraw %}

<script type="text/javascript">
    $(document).ready(function () {
        var renderDownloadStatsSrc = $("#render-download-stats-template").html();
        var renderDownloadStats = Handlebars.compile(renderDownloadStatsSrc);

        $.getJSON("https://api.github.com/repos/appleseedhq/appleseed/releases", function (releases) {
            var orderedReleases = releases.sort(function (lhs, rhs) {
                var lhsDate = Date.parse(lhs.created_at);
                var rhsDate = Date.parse(rhs.created_at);
                return lhsDate < rhsDate ? 1 :
                       lhsDate > rhsDate ? -1 : 0;
            });
            var html = renderDownloadStats(orderedReleases);
            $("#download-stats").html(html);
        });
    });
</script>
