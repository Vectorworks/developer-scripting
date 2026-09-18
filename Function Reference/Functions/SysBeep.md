# SysBeep

## Description
Procedure SysBeep uses the current system prompt sound to alert the user.

```pascal
PROCEDURE SysBeep;
```

```python
def vs.SysBeep():
    return None
```

## Examples
```pascal
SysBeep;
```
```python
vs.SysBeep()
vs.Absolute()
vs.MoveTo( 0, 0 )
vs.BeginGroup()
vs.CreateText( message1 )

if vs.PSweep > 90:
	vs.SysBeep()
	sweepTmp = 90
	vs.SetRField( gObjHandle, gObjName, 'Sweep', '90' )
```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
