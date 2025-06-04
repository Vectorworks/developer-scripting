# GetTileRepetitionPoint

## Description
Gets the specified tile resource's repetition point.

```pascal
PROCEDURE GetTileRepetitionPoint(
				tileHandle          : HANDLE;
				VAR repetitionPoint : POINT);
```

```python
def vs.GetTileRepetitionPoint(tileHandle):
    return repetitionPoint
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The tile resource from which to get the repetition point.|
|repetitionPoint|POINT|The retrieved repetition point.|

## Examples
```pascal
GetTileRepetitionPoint(tileHandle, repetitionPoint);
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
