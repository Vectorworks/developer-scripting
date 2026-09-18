# LDevice_SetAccCell

## Description
Change accessory parent cell by cell index.

```pascal
PROCEDURE LDevice_SetAccCell(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				newCellIndex   : LONGINT);
```

```python
def vs.LDevice_SetAccCell(handle, cellIndex, accessoryIndex, newCellIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|newCellIndex|LONGINT|   |

## Examples
```pascal
LDevice_SetAccCell(handle, 1, 2, 3);
```
```python
import vs

# Change accessory parent cell by cell index.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1
newCellIndex = 1

vs.LDevice_SetAccCell(handle, cellIndex, accessoryIndex, newCellIndex)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
