# GetTileOffsetPoint

## Description
Gets the specified tile resource's offset point.

```pascal
PROCEDURE GetTileOffsetPoint(
				tileHandle      : HANDLE;
				VAR offsetPoint : POINT);
```

```python
def vs.GetTileOffsetPoint(tileHandle):
    return offsetPoint
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The tile resource from which to get the offset point.|
|offsetPoint|POINT|The retrieved offset point.|

## Examples
```pascal
GetTileOffsetPoint(tileHandle, offsetPoint);
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
