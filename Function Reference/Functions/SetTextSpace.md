# SetTextSpace

## Description
Procedure SetTextSpace sets the line spacing of the referenced text object.

**Table - Text Spacing**

| Leading        | Constant |
|----------------|----------|
| Single space   | 2        |
| 1 1/2 space    | 3        |
| Double space   | 4        |

```pascal
PROCEDURE SetTextSpace(
				theText : HANDLE;
				spacing : INTEGER);
```

```python
def vs.SetTextSpace(theText, spacing):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|spacing|INTEGER|Line spacing for text.|

## Remarks
Use [SetTextLeading](SetTextLeading.md) to set a custom line spacing.

## Examples
```pascal
IF text<>'' THEN CreateText(text) ELSE CreateText(' ');
{Set correct text alignment}
SetTextVertAlignN(LNewObj, tVAlign);
SetTextJustN(LNewObj, tJust);
SetTextSpace(LNewObj, 2);
SetFPat(LNewObj,0);
GetTextOrientation(LNewObj, ptX, ptY, angle, isMirrored);
{Move the text object at the correct location}
HMove(LNewObj, x + SizeFactor - ptX, y - ptY);

CreateText(CellValue);
SetFPat(LNewObj,0);
SetTextVerticalAlign(LNewObj,1);
SetTextJust(LNewObj,1);
SetTextSpace(LNewObj,2);
END;
```
```python
import vs

# Procedure SetTextSpace sets the line spacing of the referenced text object.
theText = 'Example text'
spacing = 1

vs.SetTextSpace(theText, spacing)
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
