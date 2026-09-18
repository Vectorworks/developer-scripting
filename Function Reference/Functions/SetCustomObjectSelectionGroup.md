# SetCustomObjectSelectionGroup

## Description
Set selection indication geometry for a parametric object.

See [[VS:Parametric Custom Selection Indication]] for more info.

```pascal
FUNCTION SetCustomObjectSelectionGroup(
				objectHand : HANDLE;
				selGroup   : HANDLE): BOOLEAN;
```

```python
def vs.SetCustomObjectSelectionGroup(objectHand, selGroup):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to parametric object.|
|selGroup|HANDLE|Handle to object or group that contains geometry for selection indication.|

## Examples
```pascal
IF ( HighlightGroupHand <> NIL ) THEN boo := SetCustomObjectSelectionGroup( pioHand, HighlightGroupHand );

	boo := SetCustomObjectSelectionGroup( pioHand, HDuplicate( pioSelectGroupHand, 0, 0 ) );
END ELSE
BEGIN
	BeginGroupN( pioSelectGroupHand );
		Rect	(

IF ( MaskPolyHand[0]  <> NIL ) THEN boo := SetCustomObjectSelectionGroup( pioHand, HDuplicate( pioPathObjHand, 0, 0 ) );
```
```python
import vs

# Set selection indication geometry for a parametric object.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer
selGroup = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.SetCustomObjectSelectionGroup(objectHand, selGroup)
if ok:
    vs.Message('SetCustomObjectSelectionGroup succeeded')
else:
    vs.Message('SetCustomObjectSelectionGroup failed')
```

## Version
Availability: from Vectorworks14.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
