# SetTextSpace

## Description
Procedure SetTextSpace sets the line spacing of the referenced text object.

{| class="wikitable_c"
|+ Table - Text Spacing
! Leading !! Constant
|-
| Single space
| style="text-align:center"| 2
|-
| 1 1/2 space
| style="text-align:center"| 3
|-
| Double space
| style="text-align:center"| 4
|}

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
Use [[VS:SetTextLeading| SetTextLeading]] to set a custom line spacing.

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
