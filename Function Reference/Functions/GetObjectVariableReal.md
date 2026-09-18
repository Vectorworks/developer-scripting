# GetObjectVariableReal

## Description
Returns the value of a VectorWorks object property. Used with properties returning a REAL value. Always returns values in mm, regardless of document units.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
FUNCTION GetObjectVariableReal(
				h     : HANDLE;
				index : INTEGER): REAL;
```

```python
def vs.GetObjectVariableReal(h, index):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Examples
#### VectorScript ####
```pascal
dim_offset:= GetObjectVariableReal(h,4);
```
#### Python ####
```python
dim_offset = vs.GetObjectVariableReal(h,4)
```

```pascal
BEGIN
VPHand := GetVPGroupParent(GetParent(ParentObj));
IF (VPHand <> NIL) & (GetType(VPHand) = 122) THEN
	gLayerScaleFact := GetObjectVariableReal(GetVPGroupParent(GetParent(ParentObj)), 1003);
END;

BEGIN
	viewportRotationAngle := GetObjectVariableReal(myObjectHandle,1026);
END;

if str <> '' then BEGIN
	version := Str2Num(str);
	GetContainerInfo(parmH, containerHandle, containerType, containerScale);
	if version >= 1000 then BEGIN
		fieldVal := GetObjectVariableReal(parmH, 17) * (72.0/25.4) / containerScale;
		SetRField(parmH, parmN, fieldN, Num2Str(3, fieldVal));
	end else if (ValidNumStr(GetRField(parmH, parmN, fieldN), fieldVal)) & (fieldVal > 0) then BEGIN
		SetObjectVariableReal(parmH, 17, fieldVal * (25.4/72.0) * containerScale); {pts to world coords}
		TextSize(fieldVal);
```
```python
if containerHandle != None:
	containerScale = vs.GetObjectVariableReal( containerHandle, 1003 )
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
