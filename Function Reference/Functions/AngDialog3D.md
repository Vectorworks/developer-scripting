# AngDialog3D

## Description
Function AngDialog3D displays a dialog box which requests the user to enter three angle values. AngDialog3D will accept angle values in any supported angle format.

```pascal
PROCEDURE AngDialog3D(
				displayStr       : STRING;
				xStr             : STRING;
				yStr             : STRING;
				zStr             : STRING;
				VAR xAngleResult : REAL;
				VAR yAngleResult : REAL;
				VAR zAngleResult : REAL);
```

```python
def vs.AngDialog3D(displayStr, xStr, yStr, zStr):
    return (xAngleResult, yAngleResult, zAngleResult)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|displayStr|STRING|Dialog user prompt string.|
|xStr|STRING|Default value for input field.|
|yStr|STRING|Default value for input field.|
|zStr|STRING|Default value for input field.|
|xAngleResult|REAL|Returns user input X value.|
|yAngleResult|REAL|Returns user input Y value.|
|zAngleResult|REAL|Returns user input Z value.|

## Examples
#### VectorScript ####
```pascal
AngDialog3D('Enter the angle values:','0','0','0',x,y,z);
```
#### Python ####
```python
x,y,z = AngDialog3D('Enter the angle values:','0','0','0')
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
