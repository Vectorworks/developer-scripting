# PDF_GetPageSizeFromBlob

## Description
Takes Blob Data and returns corresponding page rect

```pascal
FUNCTION PDF_GetPageSizeFromBlob(
				inBlobPtr    : PROCEDURE;
				inBlobSize   : LONGINT;
				inPageBoxID  : LONGINT;
				inCurPage    : PROCEDURE;
				outBoxLeft   : PROCEDURE;
				outBoxTop    : PROCEDURE;
				outBoxRight  : PROCEDURE;
				outBoxBottom : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_GetPageSizeFromBlob(inBlobPtr, inBlobSize, inPageBoxID, inCurPage, outBoxLeft, outBoxTop, outBoxRight,  outBoxBottom):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inPageBoxID|LONGINT|   |
|inCurPage|PROCEDURE|   |
|outBoxLeft|PROCEDURE|   |
|outBoxTop|PROCEDURE|   |
|outBoxRight|PROCEDURE|   |
|outBoxBottom|PROCEDURE|   |

## Examples
```pascal
resultOK := PDF_GetPageSizeFromBlob(inBlobPtr, 1, 2, inCurPage, outBoxLeft, outBoxTop, outBoxRight, outBoxBottom);
```
```python
import vs

# Takes Blob Data and returns corresponding page rect.
inBlobPtr = 'Example'
inBlobSize = 1
inPageBoxID = 2
inCurPage = 'Example'
outBoxLeft = 'Example'
outBoxTop = 'Example'
outBoxRight = 'Example'
outBoxBottom = 'Example'

ok = vs.PDF_GetPageSizeFromBlob(inBlobPtr, inBlobSize, inPageBoxID, inCurPage, outBoxLeft, outBoxTop, outBoxRight, outBoxBottom)
if ok:
    vs.Message('PDF_GetPageSizeFromBlob succeeded')
else:
    vs.Message('PDF_GetPageSizeFromBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
