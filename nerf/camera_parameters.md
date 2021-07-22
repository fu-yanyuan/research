camera parameters
---  

#### Camera parameters  
in [NeRF--], camera parameters consists of intrinsic part and extrinsic part.  
> Camera intrinsics. Assuming a __pinhole camera model__, the camera intrinsic parameters can be expressed by a 3x3 matrix:  
> K [to do: add the math fomula here, equation (6) in the paper]  
> camera focal lengths along the width and height of the sensor, and the principoe points in the inmage plane.  
> (find the defination of the above)
> ####
> Camera extrinsics. the camera extrinsic parameters determine the position and orientation of the camera,  
> expressed as a transformation matrix T=[R|t]  
> explation of [SE(3)](https://zhuanlan.zhihu.com/p/88771394) in Chinese  


### NeRF   
explanation of `poses_bound.npy`  
refer to [Using your own poses without running COLMAP](https://github.com/Fyusion/LLFF#using-your-own-poses-without-running-colmap)  
```python
def load_data(arr):
    # poses_arr = np.load(os.path.join(basedir, 'poses_bounds.npy'))
    # here for simplification
    poses_arr = arr
    poses = poses_arr[:, :-2].reshape([-1, 3, 5]).transpose([1,2,0])
    bds = poses_arr[:, -2:].transpose([1,0])
    
    print(poses_arr.shape)
    print(poses_arr[1])
    print(poses.shape)
    print(poses[:,:,1])
    print(bds.shape)
    print(bds[:,1])
```  
```
# output
PS E:\python3> python test_read_npy_file.py
(34, 17)
[ 1.02612122e-02  9.99946773e-01  1.07639579e-03 -4.32800949e+00
  7.50000000e+02  9.99947014e-01 -1.02603172e-02 -8.33698611e-04
 -2.25199066e+00  1.00000000e+03 -8.22610073e-04  1.08489351e-03
 -9.99999073e-01  1.42155759e+00  8.90481487e+02  2.28278292e+01
  1.57429449e+02]
(3, 5, 34)
[[ 1.02612122e-02  9.99946773e-01  1.07639579e-03 -4.32800949e+00
   7.50000000e+02]
 [ 9.99947014e-01 -1.02603172e-02 -8.33698611e-04 -2.25199066e+00
   1.00000000e+03]
 [-8.22610073e-04  1.08489351e-03 -9.99999073e-01  1.42155759e+00
   8.90481487e+02]]
(2, 34)
[ 22.8278292  157.42944941]
```  


