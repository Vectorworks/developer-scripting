# HPerimN

## Description
Calculate a perimeter of an object. Same as HPerim(), but it gives more accurate result when the object is a polyline.

```pascal
FUNCTION HPerimN(ObjectHandle : HANDLE): REAL;
```

```python
def vs.HPerimN(ObjectHandle):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ObjectHandle|HANDLE|   |

## Examples
```pascal
perimeter := HPerimN(object);
```

```pascal
perim := HPerimN (objH);
area  := HAreaN  (objH);

BEGIN
	IF (GetTypeN(hPath)>0) THEN
		FindPathLen := HPerimN(hPath)
		ELSE
			FindPathLen := 0;
END

BEGIN
	CirNumStr := Num2Str(0,CirNum);
	SetFPat(JumperPath,0);
	JumperLength := HPerimN(JumperPath);
	{NameClass(JumperClass);}
	Jumper := CreateCustomObjectPathN(kJumperRecName,JumperPath,NIL);
	IF NOT(IsFPatByClass(Jumper)) THEN SetFPat(Jumper,0); {Default to no fill if not forced by class}
	SetRField(Jumper,kJumperRecName,'Connector Type',JumperConnectorType);
```
```python
import vs

# Calculate a perimeter of an object.
ObjectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.HPerimN(ObjectHandle)
vs.Message('HPerimN returned: ' + str(value))
```
See also in tutorials: [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Object Info](../Categories/Object%20Info.md)
