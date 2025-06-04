# Projection

## Description
Procedure Projection sets the projection mode of a VectorWorks document.

Parameters viewDistance, clip1, and clip2 are used only in perspective projection mode.

```pascal
PROCEDURE Projection(
				proj          : INTEGER;
				rMode         : INTEGER;
				viewDistance  : REAL;
				clip1X,clip1Y : REAL;
				clip2X,clip2Y : REAL);
```

```python
def vs.Projection(proj, rMode, viewDistance, clip1, clip2):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|proj|INTEGER|Projection mode of document.|
|rMode|INTEGER|Render mode of document.|
|viewDistance|REAL|View length.|
|clip1|REAL|Top left coordinate of clipping rectangle.|
|clip2|REAL|Bottom right coordinate of clipping rectangle.|

## Remarks
[[User:CBM-c-|_c_]], (2015.02.24): 

The projection mode constants (in the SDK they are called type constants):
* 0 = Orthogonal
* 1 = Perspective;
* 2 = Cavalier Oblique 45
* 3 = Cavalier Oblique 30
* 4 = Cabinet Oblique 45
* 5 = Cabinet Oblique 30
* 6 = Plan

The render mode constants:
* 0 = WireFrame
* 1 = Quick
* 2 = Solid
* 3 = Shaded Solid
* 4 = Shaded No Lines
* 5 = Final Shaded
* 6 = Final Hidden Line
* 7 = Dashed Hidden Line
* 8 = 2D Section
* 9 = 3D Section
* 11 = Open GL
* 10 = ???
* 12 = Fast Renderworks
* 13 = Fast Shadow Renderworks
* 14 = Final Renderworks
* 15 = Custom Renderworks
* 16 = Output VRML
* 17 = Artistic Renderworks
* 18 = Sketch

[[User:CBM-c-|_c_]], (2014.08.18): From John Kerr. Many thanks John!
[[File:PerspDistance.png| cente| Diagram of the perspective distance]]

[[User:CBM-c-|_c_]], (2014.08.18): this below has lost the author during one of the wiki updates:

from somebody on the VS list:
I made some tests with the following results: When I use the setting 'low perspective' (don't know the correct expression in english, sorry), it's the same as entering 24.41 for 'set perspective'. 

'normal' is the same as 9.76 and high the same as 4.88. With Projection, proj = 1, the perspective is always set to 9.76. And what I enter for viewDistance is substracted from this value. (Control: GetView:offsetZ = 9.76 - Projection:viewDistance). 

Procedure SetView:zDistance = 50, for example in perspective projection mode is the same as Projection:viewDistance = -40.24. I don't know if there are other circumstances influencing this results.

From another user: The viewDistance in the projection command is directly related to the Set Perspective menu command, though oddly, it uses a different scale. It'd be interesting to know the reasoning on that one! In my experiments...

viewDistance-&gt;equals-&gt;Set Perspective

* 800'->200
* 400'->100
* 100'->25
etc.

So perspective is 1/4 of viewDistance in feet. But perspective seems unit-less. It gets curiouser and curiouser!

From Julian Carr: Try this:

Projection(1, 0, 9.76 * UPI * LayerScale, dwgleft, dwgtop, dwgright, dwgbottom);

It has to be in real world inches, but has been discussed before. Try searching the archives.

## Examples
#### VectorScript ####
```pascal
Projection(1,2,3',-2,-2,2,2);
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD 4.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
