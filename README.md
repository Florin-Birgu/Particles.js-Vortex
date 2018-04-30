# Particles.js-Vortex

![Screenshot](https://raw.githubusercontent.com/Florin-Birgu/Particles.js-Vortex/master/screenshot.png)

Particles vortex effect created with Particles.js and glMatrix

particles.js:569
```javascript
            /* move the particle */
            if(pJS.particles.move.enable){
                var ms = pJS.particles.move.speed/2;

                if(i%3==0) {
                    //sphere
                    var point = vec3.fromValues(points[i].x, points[i].y, points[i].z);

                    var localPoint = vec3.create();
                    vec3.transformMat4(localPoint, point, m);
                    var screenPoint = vec3.create();
                    vec3.transformMat4(screenPoint, point, pvm);

                    p.x = screenPoint[0] * halfWidth + pJS.canvas.w/2;
                    p.y = screenPoint[1] * halfHeight + pJS.canvas.h/2;
                }
                else {
                    p.x += p.vx * ms;
                    p.y += p.vy * ms;
                }
            }
```

html header
```html
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gl-matrix/2.4.0/gl-matrix-min.js"></script>

```