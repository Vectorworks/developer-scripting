# IsTileGroupContainedObject

## Description
Determines if the specified object is a tile group-contained object.

```pascal
FUNCTION IsTileGroupContainedObject(objectHandle : HANDLE): BOOLEAN;
```

```python
def vs.IsTileGroupContainedObject(objectHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The object handle to check.|

## Examples
```pascal
return := IsTileGroupContainedObject(objectHandle);
```

```pascal
resultOK := IsTileGroupContainedObject(objectHandle);
```
```python
import vs

# Determines if the specified object is a tile group-contained object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsTileGroupContainedObject(objectHandle)
if ok:
    vs.Message('IsTileGroupContainedObject succeeded')
else:
    vs.Message('IsTileGroupContainedObject failed')
```

## See Also
VS Functions:
[CreateTile](CreateTile.md) 
| [ShowEditTileDialog](ShowEditTileDialog.md) 
| [ShowEditTileSettingsDialog](ShowEditTileSettingsDialog.md) 
| [ShowNewTileDialog](ShowNewTileDialog.md) 
| [GetTileGeometryGroup](GetTileGeometryGroup.md) 
| [BeginGroupN](BeginGroupN.md) 
| [AddTileGeometryObject](AddTileGeometryObject.md) 
| [GetTileGroupParent](GetTileGroupParent.md) 
| [IsTileGroupContainedObject](IsTileGroupContainedObject.md) 
| [GetTileBackgroundColor](GetTileBackgroundColor.md) 
| [SetTileBackgroundColor](SetTileBackgroundColor.md) 
| [GetTileRepetitionPoint](GetTileRepetitionPoint.md) 
| [SetTileRepetitionPoint](SetTileRepetitionPoint.md) 
| [GetTileOffsetPoint](GetTileOffsetPoint.md) 
| [SetTileOffsetPoint](SetTileOffsetPoint.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
