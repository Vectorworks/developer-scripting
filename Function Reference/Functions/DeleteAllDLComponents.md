# DeleteAllDLComponents

## Description
Deletes all components in the Double Line Preferences.

```pascal
FUNCTION DeleteAllDLComponents : BOOLEAN;
```

```python
def vs.DeleteAllDLComponents():
    return BOOLEAN
```

## Remarks
CJG 6-27-06

## Examples
```pascal
resultOK := DeleteAllDLComponents;
```
```python
import vs

# Deletes all components in the Double Line Preferences.
ok = vs.DeleteAllDLComponents()
if ok:
    vs.Message('DeleteAllDLComponents succeeded')
else:
    vs.Message('DeleteAllDLComponents failed')
```

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
