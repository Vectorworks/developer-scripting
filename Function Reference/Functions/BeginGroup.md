# BeginGroup

## Description
Procedure BeginGroup creates a new group object in a VectorWorks document. Procedure calls subsequent to BeginGroup and before EndGroup will be included in the new group object. BeginGroup may be called repeatedly to created nested groups of objects.

```pascal
PROCEDURE BeginGroup;
```

```python
def vs.BeginGroup():
    return None
```

## Examples
==== VectorScript ====
```pascal
BeginGroup;
Rect(-1,1,0.5,0);
Rect(0,1.5,1,0.5);
Oval(-1.5,0.5,-0.5,-0.5);
EndGroup;
{creates a group}

BeginGroup;
Rect(-1,1,0,0.5);
Rect(-1,0.5,-0.5,0);
BeginGroup;
Oval(-0.5,0.5,1,0);
Oval(0,0,1,-0.5);
EndGroup;
EndGroup;
{creates a group comprised of 2 rects and 1 group}
```
==== Python ====
```python
vs.BeginGroup()
vs.Rect(-1,1,0.5,0)
vs.Rect(0,1.5,1,0.5)
vs.Oval(-1.5,0.5,-0.5,-0.5)
vs.EndGroup()
#{creates a group}

vs.BeginGroup()
vs.Rect(-1,1,0,0.5)
vs.Rect(-1,0.5,-0.5,0)
vs.BeginGroup()
vs.Oval(-0.5,0.5,1,0)
vs.Oval(0,0,1,-0.5)
vs.EndGroup()
vs.EndGroup()
#{creates a group comprised of 2 rects and 1 group}
```

## Version
Availability: from All Versions

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
