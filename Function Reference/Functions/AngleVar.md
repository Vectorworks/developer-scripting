# AngleVar

## Description
Sets the angle designation method in VectorScript. When called, VectorScript will treat language symbols which can be interpreted as direction angles (e.g., N, S, NW, SE) as variables rather than angles.

```pascal
PROCEDURE AngleVar;
```

```python
def vs.AngleVar():
    return None
```

## Examples
==== VectorScript ====
```pascal
procedure test;
var
S : Real;

begin
AngleVar;
S := 30;
LineTo(3&quot;, #S);
{ The 'S' will be treated as a variable }
{ and line will be drawn on 30 degree angle. }

end;
run(test);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
