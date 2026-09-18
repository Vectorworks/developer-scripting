# PDF_PrintBlob

## Description
Prints a page from the PDF Blob

```pascal
FUNCTION PDF_PrintBlob(
				inBlobPtr  : PROCEDURE;
				inBlobSize : LONGINT;
				inSettings : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_PrintBlob(inBlobPtr, inBlobSize, inSettings):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|PROCEDURE|   |
|inBlobSize|LONGINT|   |
|inSettings|PROCEDURE|   |

## Examples
```pascal
resultOK := PDF_PrintBlob(inBlobPtr, 1, inSettings);
```
```python
import vs

# Prints a page from the PDF Blob.
inBlobPtr = 'Example'
inBlobSize = 1
inSettings = 'Example'

ok = vs.PDF_PrintBlob(inBlobPtr, inBlobSize, inSettings)
if ok:
    vs.Message('PDF_PrintBlob succeeded')
else:
    vs.Message('PDF_PrintBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
