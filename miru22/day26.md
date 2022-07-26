Share
====

Q&A about 2 works during the poster time.

### OL2B-1: squeezeNeRF
- store a small cache of the nerual network of a __trained__ NeRF to speed up inference time (not training time).
- cache size:
   - NeRF: `O(n^5)`
   - fastNeRF: `O(n^3)`
   - squeezeNeRF: `O(n^2)`
   - `n` stands for the number of querrying points(a ray for each pixel, and hundreds of such points along each ray)
   - `power` is related to each 
