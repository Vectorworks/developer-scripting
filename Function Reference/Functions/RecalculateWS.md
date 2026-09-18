# RecalculateWS

## Description
Recalculates all formulas for the referenced worksheet.

```pascal
PROCEDURE RecalculateWS(worksheet : HANDLE);
```

```python
def vs.RecalculateWS(worksheet):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|

## Remarks
This does not update the screen, so you should also do:
```pascal
ResetObject(worksheet);
WSImage := GetWSImage(worksheet);
If WSImage <> NIL then ResetObject(WSImage);
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE WSrecalc;
{ (c) Petri Sakkinen 2008, except the key part which is (c) Victor via VSFR }

VAR 
  i, n : INTEGER;
  objName : STRING;
  foundObject : HANDLE;
  OK : BOOLEAN; 

FUNCTION DoIt (h : HANDLE) : BOOLEAN;
BEGIN
  RECALCULATEWS(h);
  RESETOBJECT(h);              { these two lines   }
  RESETOBJECT(GETWSIMAGE(h));  { are the key part! }
END;

BEGIN
  n := NAMENUM; 
  FOR i := 1 TO n DO BEGIN
    foundObject := GETOBJECT(NAMELIST(i));
    IF GETTYPE(foundObject) = 18 THEN ok := DoIt(foundObject);
  END; 
END;
RUN(WSrecalc);
```
#### Python ####
```python

```

```pascal
	{Recalculate}
	RecalculateWS(tempHandle);
	ResetObject(tempHandle);
	SetObjectVariableBoolean(tempHandle,82,FALSE);
END

	SetWSCellBorder(wsHand, kFldNameRow, kLocCol, kNumRows,  kRadiusCol, TRUE,  TRUE,  TRUE,  TRUE,  TRUE);
	str := Concat('=DATABASE(INOBJECT & (R IN [''NNA_PropertyLine_CurveData''])) & (L=', QStr(GetLName(GetLayer(objHand))), ')');
	SetWSCellFormula(wsHand, kNumRows, 0, kNumRows, 0, str);
	SetWSColumnOperators(wsHand, kNumRows, -1, 0, 0, 0, 0, 0);
	RecalculateWS(wsHand);
END;

BEGIN
RecalculateWS( MyWSHandle );
SetRField(objHand, objName, 'UpdateWS', 'FALSE');
ResetObject(MyWSHandle);
WSImage := GetWSImage(MyWSHandle);
IF WSImage <> NIL THEN ResetObject(WSImage);
```
```python
vs.RecalculateWS(worksheet)
```
See also in tutorials: [21. Hello Worksheet — Create and Populate](ai%20examples/21_WorksheetBasic.md), [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [23. Count Objects by Criteria (Formula-Driven)](ai%20examples/23_WorksheetCountByCriteria.md), [24. Auto-Populating Database Row](ai%20examples/24_WorksheetDBRowAutoPopulate.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
