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

## Examples
```pascal
resultOK := PDF_GetNumOfAnnotations(inBlobPtr, 1, 2);
```
```python
import vs

# Returns the number of the PDF annotations per PDF page.
inBlobPtr = 'Example'
inBlobSize = 1
inCurPage = 2

ok = vs.PDF_GetNumOfAnnotations(inBlobPtr, inBlobSize, inCurPage)
if ok:
    vs.Message('PDF_GetNumOfAnnotations succeeded')
else:
    vs.Message('PDF_GetNumOfAnnotations failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
