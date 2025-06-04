# GetRField

## Description
Returns string description of a value in the specified record field.

```pascal
FUNCTION GetRField(
				h      : HANDLE;
				record : STRING;
				field  : STRING): DYNARRAY[] of CHAR;
```

```python
def vs.GetRField(h, record, field):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|record|STRING|Name of record format.|
|field|STRING|Name of field to be queried.|

## Remarks
(MaKro, June 2018):
To fetch the default values, use GetObject(GetName(GetParametricRecord(..))) as handle.
Object Type of GetObject return value is 47 (Record Definition) vs. 48 (Record) from GetParametricRecord.

[[User:CBM-c-|_c_]], 2015.02.24:
Please note that since the introduction of ifc data, the usual praxis of fetching plug-in records using 
 GetRecord(h, NumRecords(h))
can bring you perhaps unexpectedly the ifc record. Use [[VS:GetParametricRecord]] instead, introduced from VW 2011.

(Others): 
Returns a string interpretation of the field from the specified record

[CLC 2001/11/12]: Note that when using this to access parameter fields in a PIO, you get the values of the instance of the plug-in, not the default values, as set in the plug-in editor. If you want the default values, you have to use the handle to the PIO record format.

[CLC 2004/11/8]: This returns values rounded to the nearest display accuracy, whereas pFieldName returns the actual number.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;

FUNCTION WriteFieldValues(h :HANDLE) :BOOLEAN;
VAR
cnt     :INTEGER;
recHand :HANDLE;
recName :STRING;
fldName :STRING;
BEGIN
recName := GetName(GetRecord(h, NumRecords(h))); { ... use GetParametricRecord(h) instead }
recHand := GetObject(recName);
FOR cnt := 1 TO NumFields(recHand) DO BEGIN
fldName := GetFldName(recHand, cnt);
WriteLn(fldName, ': ', GetRField(h, recName, fldName));
END;
END;

BEGIN
ForEachObjectInLayer(WriteFieldValues, 2, 0, 4);
END;
RUN(Example);
```
==== Python ====
```python
import vs

hpio = vs.FSActLayer()
hrecdef = vs.GetParametricRecord(hpio)
recname = vs.GetName(hrecdef)  # Name of PIO in InfoPalette
hrec = vs.GetObject(recname)
fld = vs.GetFldName(hrec, 10)

vs.AlrtDialog(vs.GetTypeN(hrecdef))  # 48
vs.AlrtDialog(vs.GetTypeN(hrec))  # 47

vs.AlrtDialog('Recordname:' + recname)
vs.AlrtDialog('Default:' + vs.GetRField(hrec, recname, fld))

# ©MaKro - June 2018 ;-)
```

## Version
Availability: from VectorWorks 8.5

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
