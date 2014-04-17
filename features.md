---
layout: default
title: appleseed features
---

### Light Transport

* Distributed Ray Tracing
* Unidirectional Path Tracing
* Light Tracing
* Stochastic Progressive Photon Mapping (SPPM)

### Camera Models

* Pinhole camera
* Thin lens camera (for depth of field)
  - Support for polygonal diaphragms
* Spherical camera (to make environment maps)

### Reflection Models

* Lambertian BRDF (purely diffuse)
* Specular BRDF (perfect mirror)
* Specular BTDF (clear glass)
* Microfacet BRDFs
  - Oren-Nayar
  - Ward
  - Blinn
  - GGX
* Ashikhmin BRDF (anisotropic)
* Kelemen BRDF
* Arbitrary mixtures of BRDFs

### Light Source Models

* Point light
* Spot light
  - Support for gobos
* Directional light (infinitely far away)
* Mesh light
  - Purely diffuse
  - Cone-shaped
* Image-based lighting
* Preetham physically-based day sky
* Hosek & Wilkie physically-based day sky
* Physically based sun
