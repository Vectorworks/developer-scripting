# PtDialog3D

## Description
Procedure PtDialog3D displays a dialog box which requests the user to enter a 3D coordinate (point) value.

```pascal
PROCEDURE PtDialog3D(
				displayStr : STRING;
				xStr       : STRING;
				yStr       : STRING;
				zStr       : STRING;
				VAR xPt    : REAL;
				VAR yPt    : REAL;
				VAR zPt    : REAL);
```

```python
def vs.PtDialog3D(displayStr, xStr, yStr, zStr):
    return (xPt, yPt, zPt)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|displayStr|STRING|Dialog user prompt string.|
|xStr|STRING|Default value for input field.|
|yStr|STRING|Default value for input field.|
|zStr|STRING|Default value for input field.|
|xPt|REAL|Returns user input X value.|
|yPt|REAL|Returns user input Y value.|
|zPt|REAL|Returns user input Z value.|

## Examples
#### VectorScript ####
```pascal
PtDialog3D('Enter the 3D location:','0','0','0',x,y,z);
```
#### Python ####
```python
xPt, yPt, zPt = vs.PtDialog3D('User prompt string','0','0','0')
```

```pascal
PtDialog3D('Example', 'Example', 'Example', 'Example', 1.0, 2.0, 0.5);
```
```python
import vs

# Procedure PtDialog3D displays a dialog box which requests the user to enter
# a 3D coordinate (point) value.
displayStr = 'Example'
xStr = 'Example'
yStr = 'Example'
zStr = 'Example'

xPt, yPt, zPt = vs.PtDialog3D(displayStr, xStr, yStr, zStr)
vs.Message('PtDialog3D returned: ' + str((xPt, yPt, zPt)))
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
