# CreateCustomObjectN

## Description
Creates a custom object instance at specified location and angle of rotation.  The calling function can also set whether the pref dialog should appear.

```pascal
FUNCTION CreateCustomObjectN(
				objectName    : STRING;
				pX,pY         : REAL;
				rotationAngle : REAL;
				showPref      : BOOLEAN): HANDLE;
```

```python
def vs.CreateCustomObjectN(objectName, p, rotationAngle, showPref):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|Name of object.|
|p|REAL|Insertion point of object instance.|
|rotationAngle|REAL|Rotation angle (in degrees) of object instance.|
|showPref|BOOLEAN|Show the Object Properties dialog.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
h := CreateCustomObjectN('Door', 0, 0, 0, False);
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	h = vs.CreateCustomObjectN('Door', 0, 0, 0, False)
Example()
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
