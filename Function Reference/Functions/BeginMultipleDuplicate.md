# BeginMultipleDuplicate

## Description
Use this function in conjuction with EndMultipleDuplicate to preserve constraints on multiple duplicated objects.

```pascal
PROCEDURE BeginMultipleDuplicate;
```

```python
def vs.BeginMultipleDuplicate():
    return None
```

## Examples
[TraverseObjectsInActiveLayer](examples/TraverseObjectsInActiveLayer.md)

```pascal
BeginMultipleDuplicate;
```
```python
import vs

# Use this function in conjuction with EndMultipleDuplicate to preserve
# constraints on multiple duplicated objects.
vs.BeginMultipleDuplicate()
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[EndMultipleDuplicate](EndMultipleDuplicate.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Object Editing](../Categories/Object%20Editing.md)
