# ShowEditTileSettingsDialog

## Description
Displays the edit tile settings dialog for the specified tile.

```pascal
PROCEDURE ShowEditTileSettingsDialog(VAR tileHandle : HANDLE);
```

```python
def vs.ShowEditTileSettingsDialog(tileHandle):
    return tileHandle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The tile to display in dialog; passing a handle initialized to nil indicates that a new tile resource should be created and displayed in the dialog.|

## Examples
```pascal
ShowEditTileSettingsDialog(tileHandle);
{ displays the specified tile resource in the dialog }

tileHandle := nil;
ShowEditTileSettingsDialog(tileHandle);
{ creates a new tile resource and displays it in the dialog }
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
