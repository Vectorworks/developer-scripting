# PDF_FlushCache

## Description
Flushes all Document Cache.

```pascal
FUNCTION PDF_FlushCache : BOOLEAN;
```

```python
def vs.PDF_FlushCache():
    return BOOLEAN
```

## Examples
```pascal
resultOK := PDF_FlushCache;
```
```python
import vs

# Flushes all Document Cache.
ok = vs.PDF_FlushCache()
if ok:
    vs.Message('PDF_FlushCache succeeded')
else:
    vs.Message('PDF_FlushCache failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PDF](../Categories/PDF.md)
