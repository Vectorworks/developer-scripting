# SetRField

## Description
Assigns a new value to an existing field of a record attached to the referenced object.

```pascal
PROCEDURE SetRField(
				h      : HANDLE;
				record : STRING;
				field  : STRING;
				value  : DYNARRAY[] of CHAR);
```

```python
def vs.SetRField(h, record, field, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to a object with an attached record.|
|record|STRING|Name of record to be updated.|
|field|STRING|Name of field to be updated.|
|value|DYNARRAY[] of CHAR|New value for field.|

## Remarks
Update the RecordNode attached to object 'h' by setting the field 'field' of record format named 'record' to the value 'value'.

The object 'h' is redrawn afterward to support the symbol 'link text to record' feature.

Replaces obsolete function [[VS:Field]].

This can be used to update values in data records attached to objects, as well as to set PIO parameter values (parameter records). When setting values in parameter records, the record name is the PIO object name. Also, for the field name, use the field name as it appears in the plug-in editor's parameter dialog (such as "Draw3D"), not the internal parameter name (such as "pDraw3D").

If you set a pop-up record field of a plug-in object by using the string value of one of the pop-up list members, case counts. For instance, after inserting a Drawing Border-Arch object into a drawing, the [[VS:SetRField]] procedure was used to set the Drawing Size pop-up field to the string value 'Condoc F - Horizontal' whereas the parameter value is 'ConDoc F - Horizontal' (notice the 'd' in ConDoc.) The drawing form was not drawing correctly because of this (the default A size form was drawn.) However, the orphan value of 'Condoc F - Horizontal' (little 'd') did not show up in the pop-up list as would be expected, but 'ConDoc F - Horizontal' (big 'D') was selected even though the form was not drawn to that size.

## Examples
#### VectorScript ####
```pascal
SetRField(HandleToObject,'Part Info','Serial No.','P-4322');
```
#### Python ####
```python

```

## Version
Availability: from All Versions.

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
