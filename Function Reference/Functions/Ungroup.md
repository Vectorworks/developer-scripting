# Ungroup

## Description
Procedure Ungroup ungroups selected objects in a VectorWorks document.When Ungroup is called, any selected group objects will be destroyed, reverting to the original component objects.

```pascal
PROCEDURE Ungroup;
```

```python
def vs.Ungroup():
    return None
```

## Examples
```pascal
Ungroup;
```
```python
import vs

# When Ungroup is called, any selected group objects will be destroyed,
# reverting to the original component objects.
vs.Ungroup()
```

## Version
Availability: from All Versions

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
