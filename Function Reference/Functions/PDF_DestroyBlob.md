# PDF_DestroyBlob

## Description
After Creating and Copping Blob Data call this method to release Blob memory

```pascal
FUNCTION PDF_DestroyBlob(ioBlobPtr : PROCEDURE): BOOLEAN;
```

```python
def vs.PDF_DestroyBlob(ioBlobPtr):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ioBlobPtr|PROCEDURE|   |

## Examples
```pascal
resultOK := PDF_DestroyBlob(ioBlobPtr);
```
```python
import vs

# After Creating and Copping Blob Data call this method to release Blob memory.
ioBlobPtr = 'Example'

ok = vs.PDF_DestroyBlob(ioBlobPtr)
if ok:
    vs.Message('PDF_DestroyBlob succeeded')
else:
    vs.Message('PDF_DestroyBlob failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
