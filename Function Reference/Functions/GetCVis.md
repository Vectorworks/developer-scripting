# GetCVis

## Description
Returns the visibility status of the specified class.

```pascal
FUNCTION GetCVis(className : STRING): INTEGER;
```

```python
def vs.GetCVis(className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
Also, though a warning is generated, passing a string to a non-existent class returns 0.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
Message(GetCVis('Dimension'));
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	vs.Message(vs.GetCVis('Dimension'))
Example()
```

```pascal
IF ( ok ) & ( SupportedCl <> GetPluginString(3003){All} ) THEN BEGIN
	IF SupportedCl = GetPluginString(3000){Active} THEN
		if GetClass( H ) <> ActiveClass then ok := FALSE;
	IF SupportedCl = GetPluginString(3001){Editable}	THEN
		if GetCVis( GetClass( H ) ) = 2{garyed, i.e. non-editable} then ok := FALSE;
END;

for i := 1 to handle_cnt DO SetSelect(handles[i]);
list_cnt := 0;
for i := 1 to handle_cnt DO BEGIN
	tmpStr := GetClass(handles[i]);
	if GetCVis(tmpStr) <> 0 then BEGIN
		for j := 1 to list_cnt DO IF list[j] = tmpStr THEN j := list_cnt + 2;
		if j < list_cnt + 2 then BEGIN
			list_cnt := list_cnt + 1;
			list[list_cnt] := GetClass(handles[i]);
		END;

BEGIN
	{ConvertTo3DPolys fails if object is not visable}
	dpathHandle := HDuplicate(nurbsHandle,0,0);
	IF GetCVis(GetClass(dpathHandle)) <> 0 THEN
		SetClass(dpathHandle,noneClass);
	pathHandle := ConvertTo3DPolys(dpathHandle);
	tempH := FInGroup(pathHandle);
	vertCnt := 0;
	while tempH <> nil do BEGIN
```
```python
# make all classes visible for drawing, then set back the visibilities. (See VB-116777 why.)
classVis_Curb	=	vs.GetCVis( gCurb_Class )
if ( classVis_Curb != 0 ):
	vs.ShowClass( gCurb_Class )
```

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
