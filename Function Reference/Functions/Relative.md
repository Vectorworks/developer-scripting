# Relative

## Description
Sets the point designation method for VectorScript procedure calls. 

When this mode is active, all points specified in procedure calls are assumed to be X-Y offsets from the current graphics pen location. For example, the point designation (0,2) will move the graphics pen two vertical units away from its present location.

```pascal
PROCEDURE Relative;
```

```python
def vs.Relative():
    return None
```

## Examples
==== VectorScript ====
```pascal
Relative;
ClosePoly;
Poly(0,0,1,1,1,2,2,2,2,0);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
