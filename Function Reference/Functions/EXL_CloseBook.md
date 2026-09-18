# EXL_CloseBook

## Description
Save and closes the Excel file.

```pascal
FUNCTION EXL_CloseBook : BOOLEAN;
```

```python
def vs.EXL_CloseBook():
    return BOOLEAN
```

## Examples
```pascal
resultOK := EXL_CloseBook;
```
```python
import vs

# Save and closes the Excel file.
ok = vs.EXL_CloseBook()
if ok:
    vs.Message('EXL_CloseBook succeeded')
else:
    vs.Message('EXL_CloseBook failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
