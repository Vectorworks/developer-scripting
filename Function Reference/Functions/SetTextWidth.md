# SetTextWidth

## Description
Procedure SetTextWidth Sets the text wrapping margin width of the referenced text object.   

A call to SetTextWidth automatically activates text wrapping.

```pascal
PROCEDURE SetTextWidth(
				theText       : HANDLE;
				widthDistance : REAL);
```

```python
def vs.SetTextWidth(theText, widthDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|widthDistance|REAL|Text wrapping margin setting for text.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;

FUNCTION IncreaseTextWidth(h :HANDLE) :BOOLEAN;
BEGIN
SetTextWidth(h, GetTextWidth(h) * 1.2);
END;

BEGIN
ForEachObjectInLayer(IncreaseTextWidth, 2, 0, 4);
END;
RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[GetTextWidth](GetTextWidth.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
