# PDF_VerifyLibrary

## Description
Verifies the library is avaiable and loaded.

```pascal
FUNCTION PDF_VerifyLibrary : BOOLEAN;
```

```python
def vs.PDF_VerifyLibrary():
    return BOOLEAN
```

## Examples
```pascal
resultOK := PDF_VerifyLibrary;
```
```python
import vs

# Verifies the library is avaiable and loaded.
ok = vs.PDF_VerifyLibrary()
if ok:
    vs.Message('PDF_VerifyLibrary succeeded')
else:
    vs.Message('PDF_VerifyLibrary failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
