By [Vladislav Stanev](mailto:vstanev@nemetschek.net)

## What's that

Parametric object is like a container of VectorWorks objects. When rendering the parametric object, VectorWorks will draw the content (the inner objects inside the parametric) of the parametric object.

Hiding details allows the plug-in, that regenerates the content of the parametric, to control if each inner object should be drawn inside the parametric or not depending on the layer scale or viewport scale in which the parametric exist.

This will allow the plug-in to mark some of the inner objects so they don't appear if the layer scale of viewport scale is less than specified threshold or appear if the layer scale is above that threshold.

## Rules

The following rules are established for detailing.

Each plug-in (which describes parametric type) defines one threshold (N) for all parametric instances of that type.

Flags
* ovHideDetail(701)  -- object is to be hidden when showing details (looking close in the drawing)
* ovHideNonDetail(705) -- object is to be hidden when showing general (non-details) (looking the drawing from away)

If the current layer scale or viewport scale, there are the following situations:

* `<scale> <= N` then ovHideDetail(701) objects are drawn.
* `<scale> > N` then ovHideNonDetail(705) objects are drawn.

**Note:** Objects without any of those flags attached are always drawn.

## Setting up

To enable "Hide Details" for that parametric type your parametric plug-in should have eventing enabled.

Then you need to handle the `kObjOnInitXProperties(5)` event.

The plug-in must setup the extended properties and enable "Hide Details". To do that you have to set the following extended properties: `kObjXPropCustomHideFactor(16)`

The threshold is set as *double* value. The value specified is treated as 1:<value> scale threshold:

* 1:1 -- value = 1.0
* 1:2 -- value = 2.0
* 2:1 -- value = 0.5
* and so on

**Note:** Value 0 of `kObjXPropCustomHideFactor(16)` property is error situation and is considered as 1.

```vs
BEGIN {MAIN}
  result := GetCustomObjectInfo(objectName, objectHand, recordHand, wallHand);
  vsoGetEventInfo(theEvent, message );

  CASE theEvent OF
    5: {kObjOnInitXProperties}
    BEGIN
      { 1. Set Hide Details threshold
        All parametric objects of this type will have the threshold set here}
      result := SetObjPropDoubleVS(16, 2); {kObjXPropCustomHideFactor}
    END;
```

## Create inner objects

When creating inner objects in the parametring during the [kParametricRecalculate](SDK:Plug-in Object Events#kObjOnInitXProperties) event inside your [SDK:Plug-in Object Main Function](SDK:Plug-in Object Main Function) you need to mark those objects that have custom "Hide Details".

To demonstrate, create tree lines. The first one is normal, the second is marked with [ovHideDetail](SDK:Object Variables#ovHideDetail), and the third one with [ovHideNonDetail](SDK:Object Variables#ovHideNonDetail).

```vs
MoveTo( 0, 0 );
LineTo( 0, 100 );
hLine1 := LNewObj;

MoveTo( 30, 0 );
LineTo( 30, 100 );
hLine2 := LNewObj;

MoveTo( 60, 0 );
LineTo( 60, 100 );
hLine3 := LNewObj;

SetObjectVariableBoolean( hLine2, 701 {ovHideDetail}, TRUE );
SetObjectVariableBoolean( hLine3, 705 {ovHideNonDetail}, TRUE );
```

The result object looks like this:

1. When the layer scale is 1:1 -- greater than the example's threshold (1:2).

Drawing ovHideDetail(701) objects. See the rules above.
So the example object, the first line is drawn because it doesn't have flags set; and the second line is drawn because it is marked with ovHideDetail(701).

![ovHideNonDetailSample](images/ovHideNonDetailSample.jpg)

2. When the layer scale is 1:4 -- less than the example's threshold (1:2).

Drawing ovHideNonDetail(705) objects. See the rules above.
So the example object, the first line is drawn because it doesn't have flags set; and the third line is drawn because it is marked with ovHideNonDetail(705).

![ovHideDetailSample](images/ovHideDetailSample.jpg)
