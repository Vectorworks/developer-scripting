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

## Examples
```pascal
shadowAngle := DS_GetAngle;
shadowOpacity := DS_GetOpacity;
shadowOpByClass := DS_IsOpacityByClass;
docUnitsType := DS_GetOffsetUnit;{0 - page, 1 - document, 2 - from height}
DS_GetFillStyle( shadowFillStyle, shadowFillName, shadowColorRef);
```
```python
import vs

# Returns document shadow fill style, fill name or color index.
shadowFillStyle, shadowFillName, solidColorRef = vs.DS_GetFillStyle()
vs.Message('DS_GetFillStyle returned: ' + str((shadowFillStyle, shadowFillName, solidColorRef)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
