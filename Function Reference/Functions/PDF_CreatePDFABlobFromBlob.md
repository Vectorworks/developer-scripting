# PDF_CreatePDFABlobFromBlob

## Description
Takes Blob Data and creates a PDFA blob

```pascal
FUNCTION PDF_CreatePDFABlobFromBlob(
				inBlobPtr    : PROCEDURE;
				inBlobSize   : LONGINT;
				inPDFAFormat : LONGINT;
				ioBlobPtr    : PROCEDURE;
				ioBlobSize   : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_CreatePDFABlobFromBlob(inBlobPtr, inBlobSize, inPDFAFormat, ioBlobPtr, ioBlobSize):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inPDFAFormat|LONGINT|   |
|ioBlobPtr|PROCEDURE|   |
|ioBlobSize|PROCEDURE|   |

## Examples
```pascal
resultOK := PDF_CreatePDFABlobFromBlob(inBlobPtr, 1, 2, ioBlobPtr, ioBlobSize);
```
```python
import vs

# Takes Blob Data and creates a PDFA blob.
inBlobPtr = 'Example'
inBlobSize = 1
inPDFAFormat = 2
ioBlobPtr = 'Example'
ioBlobSize = 1.0

ok = vs.PDF_CreatePDFABlobFromBlob(inBlobPtr, inBlobSize, inPDFAFormat, ioBlobPtr, ioBlobSize)
if ok:
    vs.Message('PDF_CreatePDFABlobFromBlob succeeded')
else:
    vs.Message('PDF_CreatePDFABlobFromBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
