# SetVPCropObject

## Description
Sets the specified crop object in the specified viewport. If a crop object already exists, it will be replaced by the new object, so long as the new object is a valid crop.

```pascal
FUNCTION SetVPCropObject(
				viewportHandle : HANDLE;
				cropHandle     : HANDLE): BOOLEAN;
```

```python
def vs.SetVPCropObject(viewportHandle, cropHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|cropHandle|HANDLE|   |

## Examples
```pascal
		);
HMove( LNewObj, pioLoc.x, pioLoc.y );
SetLW( LNewObj, 0 );
SetClass( LNewObj, ClassList( 1 ) );
boo := SetVPCropObject( pioParentVPHand, LNewObj );
{
ResetBBox( pioParentVPHand );
}
{
```
```python
import vs

# Sets the specified crop object in the specified viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
cropHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.SetVPCropObject(viewportHandle, cropHandle)
if ok:
    vs.Message('SetVPCropObject succeeded')
else:
    vs.Message('SetVPCropObject failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
