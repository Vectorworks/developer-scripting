# PenLoc

## Description
Returns the current coordinate location of the graphics pen.

```pascal
PROCEDURE PenLoc(VAR pX,pY : REAL);
```

```python
def vs.PenLoc():
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|The current location of the graphics pen.|

## Remarks
(*_c_*, 2022.01.22) : To clarify, PenLoc doesn't return the current user defined mouse position (see [[VS:GetMouse]] for that), it returns the pen position during the script. Actions such as creating lines, polys etc. will cause the graphical pen internally to move. Is 2D only, In Python it returns a bidimensional tuple.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    pt : VECTOR;
BEGIN
    MoveTo(1, 234); { penLoc = 1, 234 }
    Line(100, 0); { pen position moved by 100 }
    PenLoc(pt.x, pt.y); { penLoc = 101, 234 }
    Message( pt );
END;
Run(Example);
```
#### Python ####
```python
vs.MoveTo(1, 234, 0) # penLoc = (1, 234)
vs.Line(100, 0) # pen position moved by 100
pt = vs.PenLoc() # penLoc = (101, 234)
vs.Message( str(pt) )
```

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
