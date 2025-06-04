# AddTileGeometryObject

## Description
Adds the specified object to the specified tile resource.

```pascal
FUNCTION AddTileGeometryObject(
				tileHandle   : HANDLE;
				objectHandle : HANDLE): BOOLEAN;
```

```python
def vs.AddTileGeometryObject(tileHandle, objectHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The handle to the tile resource.|
|objectHandle|HANDLE|The handle to the object to add.|

## Examples
```pascal
return := AddTileGeometryGroup(tileHandle, objectHandle);
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
