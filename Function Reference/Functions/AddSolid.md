# AddSolid

## Description
Function AddSolid creates a new solid addition object from the referenced source objects. If the operation succeeds, the source objects will then be contained within the newSolid object, as the primitives which define the CSG.

| Operation Result        | Result Code |
|------------------------|-------------|
| Success                | 0           |
| Null geometry error    | 1           |
| Geometry error         | 2           |
| Out of memory error    | 4           |
| Bad group error        | 5           |
| Invalid object type    | 6           |
| Bad input              | 20          |
| Handles not in document| 21          |

```pascal
FUNCTION AddSolid(
				obj1         : HANDLE;
				obj2         : HANDLE;
				VAR newSolid : HANDLE): INTEGER;
```

```python
def vs.AddSolid(obj1, obj2):
    return (INTEGER, newSolid)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj1|HANDLE|Handle to source object for add operation.|
|obj2|HANDLE|Handle to source object for add operation.|
|newSolid|HANDLE|Handle to resultant object from add operation.|

## Examples
[BeginXtrd](examples/BeginXtrd.md)

```pascal
BEGIN
IF (CounterTop <> NIL) & (TopReveal <> NIL) THEN
	Result := AddSolid(CounterTop,TopReveal,CounterTop);
IF (CounterTop <> NIL) & (Splash <> NIL) THEN
	Result := AddSolid(CounterTop,Splash,CounterTop);
	AttrReconfig(CounterTop,parmHand);
END;

resultcode:=AddSolid(hVault1,hVault2,hVaultComb);
resultcode:=SubtractSolid(hTower,hVaultComb,hCampi);
SetTextureRef(hCampi,-1,3);

	status := AddSolid (objH1 [1], LNewObj, objH1 [1]);
	FOR cnt := 2 TO numDividers DO
		status := AddSolid (objH1 [1], objH1 [cnt], objH1 [1]);
END;
```
```python
import vs

# Function AddSolid creates a new solid addition object from the referenced
# source objects.
obj1 = vs.FSActLayer()  # handle to the first selected object on the active layer
obj2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

resultN, newSolid = vs.AddSolid(obj1, obj2)
vs.Message('AddSolid returned: ' + str((resultN, newSolid)))
```
See also in tutorials: [06. Boolean Solids: Drill a Hole Through a Block](ai%20examples/06_BooleanSolids.md)

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
