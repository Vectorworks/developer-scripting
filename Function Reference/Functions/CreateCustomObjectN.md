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
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
h := CreateCustomObjectN('Door', 0, 0, 0, False);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	h = vs.CreateCustomObjectN('Door', 0, 0, 0, False)
Example()
```

```pascal
{create the properly rotated Callout object}
CNH := CreateCustomObjectN(kCallout, startCNV[1], startCNV[2], rotCN, FALSE);

ObjectHand := CreateCustomObjectN (kSeatingObjectName, -OriginX,-OriginY, 0, FALSE);
IF ObjectHand <> NIL THEN
BEGIN
	result := SetCustomObjectPath (ObjectHand, poly_h);
	polyClass := GetClass(poly_h);

GetPtL(pt1.x, pt1.y, pt2.x, pt2.y);
ForcePick(pt2, h2, node2, GetPlugInString(3002));
IF (node2 <> '') & (node1 <> node2) THEN BEGIN
	DSelectAll;
	h1 := CreateCustomObjectN('Flowchart Link', 0, 0, 0, FALSE);
	pt3 := pt1 + ((pt2 - pt1) / 3);
	pt4 := pt1 + ((pt2 - pt1) / 3 * 2);
	SetRField(h1, 'Flowchart Link', 'ControlPoint01X', Concat(pt3.x));
	SetRField(h1, 'Flowchart Link', 'ControlPoint01Y', Concat(pt3.y));
```
```python
import vs

# Creates a custom object instance at specified location and angle of rotation.
objectName = 'Example'
p = (0, 0)
rotationAngle = 45.0
showPref = True

objHandle = vs.CreateCustomObjectN(objectName, p, rotationAngle, showPref)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
