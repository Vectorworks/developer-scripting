# SetTextWrap

## Description
Procedure SetTextWrap sets the text wrap mode of the referenced text object.

```pascal
PROCEDURE SetTextWrap(
				theText : HANDLE;
				wrap    : BOOLEAN);
```

```python
def vs.SetTextWrap(theText, wrap):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|wrap|BOOLEAN|Text wrap setting for text.|

## Remarks
If this is set to false, it will cause the margin width to be recomputed and the text block to be reformatted. If it is set to true, the width remains the same, and text will be wrapped to fit the current margin. Use SetTextWidth to change the margin.
By default, text is created with wrapping set to false.

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
