# GetObjBoundElevation

## Description
Get the elevation of the specified bound ID relative to the object's layer.

```pascal
FUNCTION GetObjBoundElevation(
				obj     : HANDLE;
				boundID : INTEGER): REAL;
```

```python
def vs.GetObjBoundElevation(obj, boundID):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|
|boundID|INTEGER|The identifier of the story bound.|

## Remarks
Peter Vandewalle: the result is in mm.

## Examples
```pascal
BEGIN
	topHeigh    := GetObjBoundElevation( gPluginH, topBoundID  );
	botHeight   := GetObjBoundElevation( gPluginH, bottomBoundID );

{ get object's Z bounds. }
topHeight      := GetObjBoundElevation( parmHand, kTopBoundID  );
bottomHeight   := GetObjBoundElevation( parmHand, kBottomBoundID );
```
```python
import vs

# Get the elevation of the specified bound ID relative to the object's layer.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
boundID = 1

value = vs.GetObjBoundElevation(obj, boundID)
vs.Message('GetObjBoundElevation returned: ' + str(value))
```

## See Also
VS Functions:
[HasObjStoryBounds](HasObjStoryBounds.md) 
| [HasObjStoryBound](HasObjStoryBound.md) 
| [GetObjStoryBound](GetObjStoryBound.md) 
| [SetObjectStoryBound](SetObjectStoryBound.md) 
| [DelObjStoryBounds](DelObjStoryBounds.md) 
| [DelObjStoryBound](DelObjStoryBound.md) 
| [GetObjStoryBoundsCnt](GetObjStoryBoundsCnt.md) 
| [GetObjStoryBoundsAt](GetObjStoryBoundsAt.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
