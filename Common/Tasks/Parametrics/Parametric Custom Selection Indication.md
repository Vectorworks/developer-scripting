By [Vladislav Stanev](mailto:vstanev@nemetschek.net)

## What's that

When you have a parametric object in the drawing that is selected, the selection indication looks like all the inner objects of the parametric are selected.

![Normal Selection Indication](images/NormalSelectionIndication.jpg)

From VectorWorks 2009 parametric objects are capable of customizing the selection indication by providing geometry which will be used to present the selection. That geometry will not be rendered, it will just determine the selection and preselection indication.

![Custom Selection Indication](images/CustomSelectionIndication.jpg)

As you can see in the image above, when the object has custom selection you can simplify the selection indication for complex geometrical objects.

**NOTE!** The geometry that determines the selection indication is kept inside each instance.

## Creating

The plug-in creates geometry that is to be used as selection indication and puts the geometry into a special group with the call `VS:SetCustomObjectSelectionGroup`.

You can pass a handle to whatever object or handle to a group object that contains geometry.

2D geometry inside the group will be presented as 2D selection indication, and 3D object -- as 3D selection indication.

```vs
BEGIN {MAIN}
  result := GetCustomObjectInfo(objectName, objectHand, recordHand, wallHand);

  { -------------------------------------------------------
    prepare selection indication geometry}
  BeginGroup;
    { 2D selection }
    Arc( -100, 100, 0, 360 );

    { 3D selection }
    BeginXtrd( ...
      ...
    EndXtrd;
  EndGroup;

  { set selection geometry for this object }
  result := SetCustomObjectSelectionGroup( objectHand, LNewObj );
