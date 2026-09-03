# Absolute

## Description
Sets the point designation method for VectorScript procedure calls. When this mode is active, all points specified in procedure calls are assumed to be coordinate locations within the document.

```pascal
PROCEDURE Absolute;
```

```python
def vs.Absolute():
    return None
```

## Examples
#### VectorScript ####
```pascal
Absolute;
ClosePoly;
Poly(0,0,1,1,1,2,2,2,2,0);
```
#### Python ####
```python
vs.Absolute
vs.ClosePoly
vs.Poly(0,0,1,1,1,2,2,2,2,0)
```

```pascal
Absolute;
```
```python
# Draw Oval
vs.Absolute()
vs.FillPat(0)
vs.Oval( -dMmarkerSize * 0.7075, dMmarkerSize * 0.7075, dMmarkerSize * 0.7075, -dMmarkerSize * 0.7075 )

vs.SysBeep()
vs.Absolute()
vs.MoveTo( 0, 0 )
vs.BeginGroup()
vs.CreateText( message1 )
vs.SetTextVerticalAlign( vs.LNewObj(), 3 )
```

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
