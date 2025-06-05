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

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
