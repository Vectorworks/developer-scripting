# GetVPGroupParent

## Description
Gets the viewport that is the parent of specified viewport group.

```pascal
FUNCTION GetVPGroupParent(groupHandle : HANDLE): HANDLE;
```

```python
def vs.GetVPGroupParent(groupHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|groupHandle|HANDLE|handle to a viewport group (crop, annotation, etc)|

## Examples
```pascal
BEGIN
VPHand := GetVPGroupParent(GetParent(ParentObj));
IF (VPHand <> NIL) & (GetType(VPHand) = 122) THEN
	gLayerScaleFact := GetObjectVariableReal(GetVPGroupParent(GetParent(ParentObj)), 1003);
END;

BEGIN
TempHand := GetParent(parmHand);
IF TempHand <> NIL THEN  vpHand := GetVPGroupParent(TempHand);
IF vpHand <> NIL THEN TempHand := GetParent(vpHand);
LayerHand := TempHand;
IF (gSheet = '') | newLabel | GetPref(544) THEN
	gSheet := GetLName(TempHand);

{		While ( GetParent( htemp ) <> nil  ) DO htemp := GetParent( htemp );
		{Here is another way to get the annotation group handle - by global variable. [KID]}
		{It is not a perfect one too, but I prefer it to the above one for now. [KID]}
		htemp := gCurrAnnotationGroupH;
		objH := GetVPGroupParent(htemp);
		layerH := GetParent(GetVPGroupParent(htemp));
	END;
```
```python
import vs

# Gets the viewport that is the parent of specified viewport group.
groupHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetVPGroupParent(groupHandle)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
