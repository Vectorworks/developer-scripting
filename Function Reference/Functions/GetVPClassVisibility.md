# GetVPClassVisibility

## Description
Gets the visibility for the specified class in the specified viewport.

```pascal
FUNCTION GetVPClassVisibility(
				viewportHandle     : HANDLE;
				className          : STRING;
				VAR visibilityType : INTEGER): BOOLEAN;
```

```python
def vs.GetVPClassVisibility(viewportHandle, className):
    return (BOOLEAN, visibilityType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|className|STRING|   |
|visibilityType|INTEGER|   |

## Remarks
visibilityType values: 
* -1 invisible, 
* 0 visible, 
* 2 gray

## Examples
```pascal
BEGIN
	OK := GetVPClassVisibility (viewportH, ClassList (i), tempVis);
	tempVis := Abs (tempVis);
	CASE tempVis OF
		0: ShowClass (ClassList (i));
		1: HideClass (ClassList (i));

BEGIN
	OK := GetVPClassVisibility (h, ClassList (i)                      , tempInt);
	IF (tempInt = 0) | (tempInt = 2) THEN
	BEGIN
		gViewPortInfo [gNumSheets2].NumClasses := gViewPortInfo [gNumSheets2].NumClasses + 1;
		gViewPortInfo [gNumSheets2].ClassName [gViewPortInfo [gNumSheets2].NumClasses] := ClassList (i);

BEGIN
	numSelVPs := numSelVPs + 1;
	IF GetVPClassVisibility  (h, kModifierClass, visibilityType) THEN
	BEGIN
		{message (' visibilityType = ',visibilityType);}
		IF visibilityType = -1 THEN
			boo := SetVPClassVisibility (h, kModifierClass, 0)
```
```python
import vs

# Gets the visibility for the specified class in the specified viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

ok, visibilityType = vs.GetVPClassVisibility(viewportHandle, className)
vs.Message('GetVPClassVisibility returned: ' + str((ok, visibilityType)))
```

## Version
Availability: from VectorWorks 11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
