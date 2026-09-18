# NumSelectedObjects

## Description
Returns the number of selected objects in all working layers.

```pascal
FUNCTION NumSelectedObjects : LONGINT;
```

```python
def vs.NumSelectedObjects():
    return LONGINT
```

## Examples
```pascal
resultN := NumSelectedObjects;
```
```python
import vs

# Returns the number of selected objects in all working layers.
count = vs.NumSelectedObjects()
vs.Message('NumSelectedObjects returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2010

## Category
* [Selection](../Categories/Selection.md)
