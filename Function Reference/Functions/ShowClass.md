# ShowClass

## Description
Sets the visibility of the specified class to normal (visible) status.

```pascal
PROCEDURE ShowClass(className : STRING);
```

```python
def vs.ShowClass(className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Examples
#### VectorScript ####
```pascal
ShowClass('Dimension');
```
#### Python ####
```python

```

```pascal
	tmpStr := Concat(Chr(13), Chr(13), tmpStr, Chr(13), Chr(13));
	IF list_cnt > 1
		THEN tmpStr := Concat(GetPlugInString(7004), tmpStr, GetPlugInString(7005))
		ELSE tmpStr := Concat(GetPlugInString(7006), tmpStr, GetPlugInString(7007));
	if YNDialog(tmpStr) then for i := 1 to list_cnt DO ShowClass(list[i]);
END;

BEGIN
NameClass(NewClass[I,1]);
ShowClass(NewClass[I,1]);
IF kDebug THEN Writeln('New : ',NewClass[I,1]);
END

	gSketchSymHandle := NIL;
END;
gUserOrigClass := ActiveClass;  {Store the user's current active class}
NameClass(kRLClass);  {Switch to / create the redlines class}
ShowClass(kRLClass);
```
```python
if ( classVis_Curb != 0 ):
	vs.ShowClass( gCurb_Class )
```

## See Also
VS Functions:
[HideClass](HideClass.md)

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
