BlenderFractals
===============

This plugin for Blender plugin allows to create 3D fractals within Blender.
As of now, two different types of fractals can be created, namely MandelBulbs and 4D JuliaSets.

Installation
------------

After downloading/cloning the repository, copy the fractals.py to
```
/.../Blender/2.xx/scripts/addons/
´´´
Then, active the plugin in Blender by navigating to the *Addons* tab located at *Files -> User Preferences*.
Find the plugin (for example by filtering for 'Add Mesh') and activate it by checking its checkbox.

Now, the interface can be found in the Toolbox on the left side of the 3D View.


Usage
-----
These settings can be changed to obtain differently looking fractals:
### Global Settings
* Factal name: name of the fractal
* p0, p1: Points within the cube spanned by these two coordinates for convergence, that is whether they belong to the fractal set or not.
* Step Size: Distance along one axis between two coordinates. ** Warning: ** The runtime of the generation algorithm scales cubicly with this parameter, so change with causion! Lower values yield finer resolved fractals.

### 4D Julia Set:
* Max Iterations: Maximum number of iterations one point is checked for convergence. Higher values yield more detailed fractals, however, computation time increases.
* Bailout Value: Value at which a point is discarded as not belonging to the fractal set. Only values <= 2 make sense since 4D JuliaSets only converge within this range.
* c: Constant to be tested defined as Quaternion.
* w projection value: Defines the projection cube of the 4D -> 3D dimensionality reduction.

### MandelBulb:
* Max Iterations: Maximum number of iterations one point is checked for convergence. Higher values yield more detailed fractals, however, computation time increaes.
* Bailout Value: Value at which a point is discarded as not belonging to the fractal set.
* Power: Power of the Mandelbulb.

