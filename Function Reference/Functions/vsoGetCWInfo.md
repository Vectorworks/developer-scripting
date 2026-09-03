# vsoGetCWInfo

## Description
Gets the information about the panel and position of an object being inserted by the curtain wall tool

```pascal
PROCEDURE vsoGetCWInfo(
				VAR width   : REAL;
				VAR height  : REAL;
				VAR centerX : REAL;
				VAR centerY : REAL;
				VAR index   : INTEGER);
```

```python
def vs.vsoGetCWInfo():
    return (width, height, centerX, centerY, index)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|width|REAL|   |
|height|REAL|   |
|centerX|REAL|   |
|centerY|REAL|   |
|index|INTEGER|   |

## Examples
```pascal
vsoGetCWInfo(1.0, 2.0, 0.5, 1.5, 1);
```
```python
import vs

# Gets the information about the panel and position of an object being
# inserted by the curtain wall tool.
width, height, centerX, centerY, index = vs.vsoGetCWInfo()
vs.Message('vsoGetCWInfo returned: ' + str((width, height, centerX, centerY, index)))
```

## Version
Availability: from Vectorworks 2015

## Category
* [Object Events](../Categories/Object%20Events.md)
