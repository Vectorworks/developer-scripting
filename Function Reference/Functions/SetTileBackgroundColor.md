# SetTileBackgroundColor

## Description
Sets the specified tile resource's background color.

```pascal
PROCEDURE SetTileBackgroundColor(
				tileHandle      : HANDLE;
				backgroundColor : LONGINT);
```

```python
def vs.SetTileBackgroundColor(tileHandle, backgroundColor):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The tile resource in which to set the background color.|
|backgroundColor|LONGINT|The RGB background color to set.|

## Examples
```pascal
SetTileBackgroundColor(tileHandle, backgroundColor);
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
