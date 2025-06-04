# DS_GetFillStyle

## Description
Returns document shadow fill style, fill name or color index.

```pascal
PROCEDURE DS_GetFillStyle(
				VAR shadowFillStyle : INTEGER;
				VAR shadowFillName  : STRING;
				VAR solidColorRef   : LONGINT);
```

```python
def vs.DS_GetFillStyle():
    return (shadowFillStyle, shadowFillName, solidColorRef)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|shadowFillStyle|INTEGER|   |
|shadowFillName|STRING|   |
|solidColorRef|LONGINT|   |

## Version
Availability: from Vectorworks 2014

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
