# ShowNewTileDialog

## Description
Displays the new tile dialog.

```pascal
FUNCTION ShowNewTileDialog : HANDLE;
```

```python
def vs.ShowNewTileDialog():
    return HANDLE
```

## Examples
```pascal
tileHandle := ShowNewTileDialog;
```

```pascal
resultH := ShowNewTileDialog;
```
```python
import vs

# Displays the new tile dialog.
objHandle = vs.ShowNewTileDialog()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
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
