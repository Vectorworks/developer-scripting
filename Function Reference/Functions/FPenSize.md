# FPenSize

## Description
Function FPenSize returns the active pen size setting (in mils).

```pascal
FUNCTION FPenSize : INTEGER;
```

```python
def vs.FPenSize():
    return INTEGER
```

## Examples
#### VectorScript ####
```pascal
CurrPenSize:=FPenSize;
```
#### Python ####
```python
CurrPenSize = vs.FPenSize()
```

```pascal
resultN := FPenSize;
```
```python
currPenSize	= vs.FPenSize()
if not vs.PShow_Joints:
	# Lines are drawn later because of joints
	vs.PenSize( 0 )
```

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
