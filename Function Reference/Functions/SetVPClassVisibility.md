# SetVPClassVisibility

## Description
Sets the visibility for the specified class in the specified viewport.

```pascal
FUNCTION SetVPClassVisibility(
				viewportHandle : HANDLE;
				className      : STRING;
				visibilityType : INTEGER): BOOLEAN;
```

```python
def vs.SetVPClassVisibility(viewportHandle, className, visibilityType):
    return BOOLEAN
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
	FOR j := 1 TO gViewPortInfo [sheetNum].NumClasses DO
		OK := SetVPClassVisibility (viewportH, gViewPortInfo [sheetNum].ClassName [j], gViewPortInfo [sheetNum].ClassVisibility [j]);
END

BEGIN
	{message (' visibilityType = ',visibilityType);}
	IF visibilityType = -1 THEN
		boo := SetVPClassVisibility (h, kModifierClass, 0)

	ELSE boo := SetVPClassVisibility (h, kModifierClass, -1);
END;

BEGIN
	OK := SetVPClassVisibility (viewportH, ClassList (i), GetCVis (ClassList (i)));
	IF frontH <> NIL THEN OK := SetVPClassVisibility (frontH, ClassList (i), GetCVis (ClassList (i)));
	IF rightH <> NIL THEN OK := SetVPClassVisibility (rightH, ClassList (i), GetCVis (ClassList (i)));
END
```
```python
import vs

# Sets the visibility for the specified class in the specified viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
visibilityType = 0

ok = vs.SetVPClassVisibility(viewportHandle, className, visibilityType)
if ok:
    vs.Message('SetVPClassVisibility succeeded')
else:
    vs.Message('SetVPClassVisibility failed')
```

## Version
Availability: from VectorWorks 11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
