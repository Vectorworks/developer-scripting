By [Vladislav Stanev](mailto:vstanev@nemetschek.net)

## What's that

When you have a parametric object put inside a wall, the wall creates an opening by the convex hull polygon in 2D and convex hull cube in 3D, created by the 2D and 3D geometry of the parametric.

![Normal Wall Opening](images/NormalWallOpening.jpg)

From VectorWorks 2009, parametric objects are capable of customizing the opening that the parametric object will cut into the wall when placed inside.

![Custom Wall Opening](images/CustomWallOpening.jpg)

The opening is customizable only in 3D.

The opening is created by a boolean operation with the 3D geometry specified from the parametric object and the wall 3D body.

**NOTE!** The geometry that determines the selection indication is kept inside each instance. The custom opening is definable only in 3D.

## Creating

The plug-in creates geometry that is to be used as opening cutting geometry and puts it into a special group with the call `VS:GetCustomObjectWallHoleGroup`.

You can pass a handle to whatever 3D object or handle to a group object that contains 3D geometry.

```vs
BEGIN {MAIN}
  result := GetCustomObjectInfo(objectName, objectHand, recordHand, wallHand);

  { -------------------------------------------------------
    Custom wall opening
    create extrude for cutting the wall
    NOTE: The plug-in must ensure that the cutting 3D geometry
    goes all the way through the wall.
  }
  BeginXtrd( -1000, 1000 );
    AddPoint( -100,-100 );
    AddPoint(  0,-50 );
    AddPoint( 100,-100 );
    AddPoint( 100,100 );
    AddPoint( 0,50 );
    AddPoint( -100,100 );
  EndXtrd;

  { set the cutting geometry }
  result := SetCustomObjectWallHoleGroup( objectHand, LNewObj );
```

The way it works is that the plug-in provides 3D geometry that is used to cut through the wall.

![Details Wall Opening](images/DetailsWallOpening.jpg)

This way the plug-in parametric object can control the opening. Do recess and sloped openings. Also, if you specify a group containing several 3D bodies, you can create separate independent openings in the wall for this parametric.

## User Comments

The code above needs `set3Drot(LNewObj,90,0,0,0,0,0);` in order to cut the shape shown in the image, as the polygon used in the extrusion would get created on the drawing's ground plane and not on the wall face.

Also, a pair of 2D loci can be used to define the 2D portion of the cut. If more than those 2 loci exist in the PIO, the "cutting" loci need to be at the bottom of the stacking order.
