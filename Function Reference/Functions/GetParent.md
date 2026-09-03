# GetParent

## Description
Returns a handle to the parent container object of the referenced object. If the object does not have a container, a handle to the objects' layer will be returned.

```pascal
FUNCTION GetParent(h : HANDLE): HANDLE;
```

```python
def vs.GetParent(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
This is from the SDK documentation for ParentObject():

Returns the "parent" of h, that is, h's immediate owner.  For most objects, this is the layer they are in; for an object in a container, it is its enclosing container; for a layer, it is the drawing header.  The drawing header and any symbol definitions which are not in any folder have no parent; calling ParentObject on them will return nil.

## Examples
```pascal
BEGIN
	ObjParent := GetParent(parmHand);
	if IsLineBasedWall(ObjParent) then
	BEGIN
		bsb := GetObjectWallOffset( parmHand, wallHand, offsetDist );
		bsb := SetObjectWallOffset( parmHand, wallHand, offsetDist + gLength);

{ making preview. }
IF( ( GetParent( gPluginH ) = NIL ) | ( gOAHeight = 0 ) | ( p__IsPilaster ) ) THEN
BEGIN
	gOAHeight := pOA_Height;
END;

BEGIN
	while ( tempH <> NIL ) & ( GetParent( tempH ) = objH ) & ( bProceed ) do BEGIN
		gType := GetType( tempH );
		IF (gType = 2{Line}) | (gType = 3{Rect}) | (gType = 5{POLYGON}) | (gType = 6{Arc}) | (gType = 21{POLYLINE}) THEN BEGIN
			if (gType = 2{Line}) then BEGIN
				GetObjArrow( tempH, style, size, Angle, bstart, bend );
				if ( not bstart ) then BEGIN
```
```python
strRecordName = kStrRecordName
strParentName = ''
parentParametric = vs.GetParent(gObjHandle)
if (parentParametric != None) and (vs.GetTypeN(parentParametric) == kPlugInObject):
	parentRecord = vs.GetRecord(parentParametric, 1)
	if (parentRecord != None) and (vs.GetTypeN(parentRecord) == kRecordNode):
		strParentName = vs.GetName(parentRecord)

while ( objH != None ) and ( vs.GetTypeN( objH ) != kLayerHeaderType ) and ( vs.GetTypeN( objH ) != kNILType ):
	containerHandle = objH
	objH = vs.GetParent( objH );
```

## Version
Availability: from VectorWorks8.5

## Category
* [Object Info](../Categories/Object%20Info.md)
