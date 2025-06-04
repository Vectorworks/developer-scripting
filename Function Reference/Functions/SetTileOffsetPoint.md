# SetTileOffsetPoint

## Description
Sets the specified tile resource's offset point.

```pascal
PROCEDURE SetTileOffsetPoint(
				tileHandle  : HANDLE;
				offsetPoint : POINT);
```

```python
def vs.SetTileOffsetPoint(tileHandle, offsetPoint):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The tile resource in which to set the offset point.|
|offsetPoint|POINT|The offsets point to be set.|

## Examples
```pascal
SetTileRepetitionPoint(tileHandle, offsetPoint);
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
