# Terra 
Commits are [here](https://www.github.com/c4stan/terra).  
This is a mirror.

### Features
- Monte Carlo unidirectional integrator
- Accelerators (BVH, KD-tree)
- BSDF presets:
    - Diffuse (importance sampled cosine weighted)
    - Microfacet layered CT glossy (importance sampled)
    - Glass (RR reflection/refraction)
    - Easy to add custom
- Texturing and HDR environment mapping
- Multiple importance sampling (direct light sampling)
- Russian Roulette for path termination
- Antialiasing via random sub-pixel jittering
- Multithread ready (see Satellite viewer)
- Incremental rendering
- Multiple (local) tonemapping operators (Linear, Reinhard, Filmic & Uncharted2)

## Sample Renderings
#### Stanford dragon ~300k triangles (BSDF: Glass)
##### Specs
**Disclamer** 8 worker threads are used in addition to the main thread, this is not an optimal scenario.
Machine: Intel Core i7-2600 @ 3.40GHz - Windows 10 Pro x64
Worker threads: 8 (1 per virtual core)

##### Stats
- `terra_trace()` ~4.2 ns
- Total Throughput ~ 1'670'000 spp

![](http://i.imgur.com/w4rndg8.jpg)

##### PBR Wood log (Textures: albedo/roughness/metalness) ~16k triangles (BSDF: Diffuse + Microfacet Specular)
![](http://i.imgur.com/jAwVDVg.jpg)

##### Stanford bunny ~70k triangles (BSDF: Diffuse + Microfacet Specular)
![](http://i.imgur.com/N6FEfsB.jpg)
