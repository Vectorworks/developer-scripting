# SetToolWithMode

## Description
Activates the specified Vectorworks tool for use with specified tool mode. The tool remains selected as the active tool after use.

```pascal
PROCEDURE SetToolWithMode(
				toolIndex  : INTEGER;
				modeGroup  : LONGINT;
				modeButton : LONGINT);
```

```python
def vs.SetToolWithMode(toolIndex, modeGroup, modeButton):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolIndex|INTEGER|Vectorworks tool constant.|
|modeGroup|LONGINT|Index of the mode group.|
|modeButton|LONGINT|Index of the button in the group.|

## Version
Availability: from Vectorworks 2016

## Category
* [Utility](../Categories/Utility.md)
