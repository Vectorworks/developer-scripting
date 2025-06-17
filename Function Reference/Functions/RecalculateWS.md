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
If WSImage &lt;&gt; NIL then ResetObject(WSImage);
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

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
