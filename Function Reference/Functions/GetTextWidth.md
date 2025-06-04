# GetTextWidth

## Description
Procedure GetTextWidth returns the margin width of the referenced text object.

```pascal
FUNCTION GetTextWidth(theText : HANDLE): REAL;
```

```python
def vs.GetTextWidth(theText):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|

## Remarks
For wrapped blocks, the margin width is that set by the user. For unwrapped blocks, it is computed by VW to be the width of the longest line.

## See Also
VS Functions:
[SetTextWidth](SetTextWidth.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
