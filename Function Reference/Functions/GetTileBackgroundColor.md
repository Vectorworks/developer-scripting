# GetTileBackgroundColor

## Description
Gets the specified tile resource's background color.

```pascal
PROCEDURE GetTileBackgroundColor(
				tileHandle : HANDLE;
				VAR red    : LONGINT;
				VAR green  : LONGINT;
				VAR blue   : LONGINT);
```

```python
def vs.GetTileBackgroundColor(tileHandle):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tileHandle|HANDLE|The tile resource from which to get the background color.|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Examples
```pascal
GetTileBackgroundColor(tileHandle, backgroundColor);
```

```pascal
GetTileBackgroundColor(tileHandle, 1, 2, 3);
```
```python
import vs

# Gets the specified tile resource's background color.
tileHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

red, green, blue = vs.GetTileBackgroundColor(tileHandle)
vs.Message('GetTileBackgroundColor returned: ' + str((red, green, blue)))
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
