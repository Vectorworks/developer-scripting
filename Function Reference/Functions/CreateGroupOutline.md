# CreateGroupOutline

## Description
Returns a handle to the polygon which is the outline of a group.

```pascal
FUNCTION CreateGroupOutline(objectHandle : HANDLE): HANDLE;
```

```python
def vs.CreateGroupOutline(objectHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|HANDLE|   |

## Examples
```pascal
BEGIN
	GetSymLoc( gMyHand, Xtemp, Ytemp );
	angle := GetSymRot( gMyHand );
	gOutlineH := CreateGroupOutline( gMyHand );
	vertex_i := GetVertNum( gOutlineH );
```
```python
import vs

# Returns a handle to the polygon which is the outline of a group.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CreateGroupOutline(objectHandle)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
