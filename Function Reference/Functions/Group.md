# Group

## Description
Procedures Group groups selected objects in a VectorWorks document. Any selected objects on the active layer(or any selected objects in the document when in Show-Snap-Modify mode) will be included in the new group object.

```pascal
PROCEDURE Group;
```

```python
def vs.Group():
    return None
```

## Examples
==== VectorScript ====
```pascal
Rect(-1,1,0,0);
Rect(-1,-0.5,0,-1.5);
Group;
{groups the most recently created objects}
```
==== Python ====
```python
vs.Rect(-1,1,0,0)
vs.Rect(-1,-0.5,0,-1.5)
vs.Group()
#{groups the most recently created objects}
```

## Version
Availability: from All Versions

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
