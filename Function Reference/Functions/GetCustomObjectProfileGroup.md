# GetCustomObjectProfileGroup

## Description
Returns a handle to the profile group of a path custom object.

A path object has two &quot;containers&quot; for storing subordinate objects: the path, and the profile. As an example, if a path object is going to do an extrude along path, it will store the path in the path container, and the shape to be extruded in the profile container. The code within the object will then supply the handles to the path and the profile to the CreateExtrudeAlongPath call.

```pascal
FUNCTION GetCustomObjectProfileGroup(objectHand : HANDLE): HANDLE;
```

```python
def vs.GetCustomObjectProfileGroup(objectHand):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to path custom object.|

## Examples
```pascal
BEGIN
	ProfileHand := GetCustomObjectProfileGroup(pluginH);
	TmpStartMarkerHand := NIL;
	GetGroups;
	{Backstop if something deletes the profile group and pick up the user defaults}
	{Check to see if we have a marker}

gFootprintIdx := getIndex(gMyName,'p2Ddisplay',p2Ddisplay);
gTagIdx := getIndex(gMyName,'pTagDisplay',pTagDisplay);
gEaveIdx := GetIndex(gMyName,'pEaveStyle',pEaveStyle);
EmptyProfileGroup := FALSE;
IF (gMyHand = NIL)  | (GetCustomObjectProfileGroup(gMyHand) = NIL) | (fInGroup(GetCustomObjectProfileGroup(gMyHand)) = NIL) THEN EmptyProfileGroup := TRUE;

BEGIN
	h := GetCustomObjectProfileGroup( objHand );
	IF h <> NIL THEN
		DelObject( h );
END
```
```python
import vs

# Returns a handle to the profile group of a path custom object.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetCustomObjectProfileGroup(objectHand)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[SetCustomObjectProfileGroup](SetCustomObjectProfileGroup.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
