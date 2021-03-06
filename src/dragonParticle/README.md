## Dragon particles
![Pixi-Particles](public/img/dragon.gif)

This sample code demonstrates some particles effects added to a tween effect.

### How does it work?

The principle is easy: we use the *svg path* values to get (x,y) values for our particle emitter.

The tweening effect will just make the particle emitter follow the (x,y) points.

We display a picture of the dragon on top to give the impression, it is actualy sparkling!

## Additional information

The svg path for the dragon is stored in index.html in a div with it's id set to `motionPath` containing a svg node. 

```html
  <div id="motionPath">
    <svg width="842px" height="596px" >
    <path fill="#FFFFFF" d="M323.587,152.743c-11.562,-0.222 -20.376,-1.334 -19.67,-3.324c3.879,-10.889 -2.155,-21.52 0.546,-21.175c4.907,0.577 9.28,1.016 13.291,1.333c-13.203,-9.955 -14.12,-18.019 -15.877,-36.097c0,0 -8.476,-11.493 -37.436,5.2c16.261,-21.893 31.431,-16.693 34.362,-15.543c0.201,-2.471 -4.051,-3.994 -13.073,-11.694c15.343,7.211 24.45,6.321 24.45,6.321c-0.111,-0.556 0.369,-6.801 -3.854,-9.372c-0.295,-0.161 -0.455,-0.253 -0.455,-0.253c0.157,0.08 0.309,0.164 0.455,0.253c2.607,1.427 15.749,8.292 22.098,5.349c9.396,-4.338 30.944,10.315 42.781,5.373c2.327,-0.977 -1.236,4.367 0.546,7.901c-1.954,5.488 -37.006,18.848 -48.67,15.371c-3.592,25.829 30.023,20.083 44.906,25.542l-0.004,0.001c5.509,2.189 5.755,19.644 -1.691,21.519c-5.894,1.478 -14.858,2.462 -24.168,2.958c0.279,3.232 -3.452,17.625 -28.094,60.997c0,0 10.445,-28.57 9.557,-60.66Z" style="fill:#1292ff;"/></svg>  
  </div>
```

and the values are retrieved using 

```fsharp
let path = anime.Globals.path(!!"#motionPath path")
```