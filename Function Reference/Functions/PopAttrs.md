# PopAttrs

## Description
Restores the attribute, tool, and constraint settings saved by an earlier call to PushAttrs.

```pascal
PROCEDURE PopAttrs;
```

```python
def vs.PopAttrs():
    return None
```

## Remarks
Calling this procedure more times than PushAttrs has been called during the execution of the script will crash VectorWorks.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
PushAttrs;
PenFore(215);
PenBack(5);
PenPat(25);
PenSize(42);
PenPat(25);
SetConstrain('q');
CallTool(-201);
PopAttrs;
END;
RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[PushAttrs](PushAttrs.md)

## Version
Availability: from MiniCAD4.0

## Category
* [Command](../Categories/Command.md)
