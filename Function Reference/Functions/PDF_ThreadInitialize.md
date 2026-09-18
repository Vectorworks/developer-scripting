# PDF_ThreadInitialize

## Description
The library needs to be Initialized per thread

```pascal
FUNCTION PDF_ThreadInitialize : BOOLEAN;
```

```python
def vs.PDF_ThreadInitialize():
    return BOOLEAN
```

## Examples
```pascal
resultOK := PDF_ThreadInitialize;
```
```python
import vs

# The library needs to be Initialized per thread.
ok = vs.PDF_ThreadInitialize()
if ok:
    vs.Message('PDF_ThreadInitialize succeeded')
else:
    vs.Message('PDF_ThreadInitialize failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
