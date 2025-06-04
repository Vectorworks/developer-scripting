# ShowEditTileDialog

## Description
Displays the edit tile dialog for the specified tile allowing the user to specify whether they wish to edit the tile's geometry or settings.

```pascal
PROCEDURE ShowEditTileDialog(tileHandle : HANDLE);
```

```python
def vs.ShowEditTileDialog(tileHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The tile for which the dialog should be displayed.|

## Examples
```pascal
ShowEditTileDialog(tileHandle);
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
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
