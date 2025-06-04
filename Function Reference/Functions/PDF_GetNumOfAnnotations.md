# PDF_GetNumOfAnnotations

## Description
Returns the number of the PDF annotations per PDF page

```pascal
FUNCTION PDF_GetNumOfAnnotations(
				inBlobPtr  : PROCEDURE;
				inBlobSize : LONGINT;
				inCurPage  : LONGINT): BOOLEAN;
```

```python
def vs.PDF_GetNumOfAnnotations(inBlobPtr, inBlobSize, inCurPage):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inCurPage|LONGINT|   |

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
