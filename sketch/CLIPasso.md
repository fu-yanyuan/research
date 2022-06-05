CLIPasso
--- 
Project web: [CLIPasso](https://clipasso.github.io/clipasso/). 
this method from SIGGRAPH 2022,  produces very abstarct results.   
Let's have a more detailed look at it and to learn more about recent sketching methods.  

----------

## CLIPASSO: Semantically-Aware Object Sketching 
a method that ultilize [CLIP](https://github.com/fu-yanyuan/research/blob/main/Papers/CLIP.md) for abstraction. 
CLIPdraw [link]() may also help.  


1. strokes are Bezier curves. More about [Bezier curvers](https://zhuanlan.zhihu.com/p/464686081) in zhihu.   
2. use [differentiable rasterizer](https://people.csail.mit.edu/tzumao/diffvg/) to optimize the parameters of strokes(Bezier curves).  



### Sketch generation methods  

1. edge map extraction methods. 
    based on geometry. (like edge detection? purely math and geometry.) 
2. free-hand sketch generation  
    more abstract. 
3. domain translation task
    simply transfer does not work. need some sketch-specific adjustments.
