# SetClass

## Description
Procedure SetClass assigns a class to the referenced object.

```pascal
PROCEDURE SetClass(
				h         : HANDLE;
				className : STRING);
```

```python
def vs.SetClass(h, className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|className|STRING|Name of class to assign to object.|

## Remarks
If you use SetClass to set the class of an object to the 'None' class, and the 'None' class has been renamed, there are two possible outcomes. If the user has renamed the 'None' class, and then created a new class named 'None' (bad idea, by the way), the class of the object will be set to 'None'. If there is not actually a class named 'None', the class of the object will be set to the original 'None' class, whatever it is named now.

Note that if a handle to group is used, all objects within the group will receive the same class assignment as the group [Julian].

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
SetClass(FSActLayer, 'None');
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
BEGIN
	gClassN := getClass( gLine );
	SetClass( gParmH, gClassN );
	{ When creating the object, SetClass regenerates it in Screen Plane.
		TO fix this we will SET it in the same plane with the gLine }
	planarRef := GetPlanarRef( gLine );
	SetPlanarRef( gParmH, planarRef );

BEGIN
	{SetRField(hObj, kRedlinePathObjName, kRedlinePathObjMemoField, gErrStr);}
	SetRField(hObj, kRedlinePathObjName, kRedlinePathObjPickedUpField, Concat(FALSE));
	SetClass(hObj, GetClass(hObj));
END

SetClass (objectH, class);
```
```python
vs.SetClass(hDuplicated, activeClName);

if objClass != "":
	vs.SetClass( objH, objClass )
	SetAttrsByClass( objH, setLineWeight )
	if t == vs.kGroupNode:
		# recursively traverse the groups as the pen and fill set doesnt work on groups
		childObjH = objH.first
```

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
