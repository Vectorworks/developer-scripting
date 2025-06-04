# EndGroup

## Description
Procedure EndGroup completes the creation of a new group object in a VectorWorks document. The new group object is then generated in the document.

```pascal
PROCEDURE EndGroup;
```

```python
def vs.EndGroup():
    return None
```

## Examples
#### VectorScript ####
```pascal
BeginGroup;
Rect(-1,1,0.5,0);
Rect(0,1.5,1,0.5);
Oval(-1.5,0.5,-0.5,-0.5);
EndGroup;
{creates a group object}

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
#### Python ####
```python
vs.BeginGroup()
vs.Rect(-1,1,0.5,0)
vs.Rect(0,1.5,1,0.5)
vs.Oval(-1.5,0.5,-0.5,-0.5)
vs.EndGroup()
#{creates a group object}

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

## See Also
VS Functions:
[BeginGroup](BeginGroup.md) | [BeginGroupN](BeginGroupN.md)

## Version
Availability: from All Versions

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
