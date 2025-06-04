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

## Version
Availability: from Vectorworks 2015

## Category
* [Object Events](../Categories/Object%20Events.md)
