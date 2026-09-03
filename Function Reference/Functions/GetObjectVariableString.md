# GetObjectVariableString

## Description
Returns the value of a VectorWorks object property. Used with properties returning a STRING value.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
FUNCTION GetObjectVariableString(
				h     : HANDLE;
				index : INTEGER): STRING;
```

```python
def vs.GetObjectVariableString(h, index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Examples
#### VectorScript ####
```pascal
dimstdName:= GetObjectVariableString(h,27);
```
#### Python ####
```python
dimstdName = vs.GetObjectVariableString(h,27)
```

```pascal
BEGIN
IF GetObjectVariableString(TempH1,kVPLocatorVar) <> '' THEN
	SetRField(ActiveParmHand,ActiveRecName,kNNA_ItemName,GetObjectVariableString(TempH1,kVPLocatorVar));
SetRField(ActiveParmHand,ActiveRecName,kNNA_SheetName, GetLName(GetLayer(TempH1)));
END;

BEGIN
vpTitle := GetObjectVariableString(vpHand, 1032);
gTitle := vpTitle;
END;

BEGIN
	returnPos := 0;
	currFieldValue := GetRField(pluginH, recordName, fieldName);
	newFieldValue := GetObjectVariableString(pluginLayer, 159);
```
```python
import vs

# Returns the value of a VectorWorks object property.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

text = vs.GetObjectVariableString(h, index)
vs.Message('GetObjectVariableString returned: ' + str(text))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
