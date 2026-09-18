# PDF_SetPageImage

## Description
Creates image of the passed PDF page object and attaches it into it's child

```pascal
FUNCTION PDF_SetPageImage(inBlobPtr : HANDLE): BOOLEAN;
```

```python
def vs.PDF_SetPageImage(inBlobPtr):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inBlobPtr|HANDLE|   |

## Examples
```pascal
resultOK := PDF_SetPageImage(inBlobPtr);
```
```python
import vs

# Creates image of the passed PDF page object and attaches it into it's child.
inBlobPtr = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.PDF_SetPageImage(inBlobPtr)
if ok:
    vs.Message('PDF_SetPageImage succeeded')
else:
    vs.Message('PDF_SetPageImage failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
