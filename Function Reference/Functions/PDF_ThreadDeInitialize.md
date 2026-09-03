# PDF_ThreadDeInitialize

## Description
When the thread completes clean up library usage

```pascal
FUNCTION PDF_ThreadDeInitialize : BOOLEAN;
```

```python
def vs.PDF_ThreadDeInitialize():
    return BOOLEAN
```

## Examples
```pascal
resultOK := PDF_ThreadDeInitialize;
```
```python
import vs

# When the thread completes clean up library usage.
ok = vs.PDF_ThreadDeInitialize()
if ok:
    vs.Message('PDF_ThreadDeInitialize succeeded')
else:
    vs.Message('PDF_ThreadDeInitialize failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
