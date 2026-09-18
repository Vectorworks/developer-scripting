# HideClass

## Description
Sets the class visibility of the specified class to hidden (invisible) status.

```pascal
PROCEDURE HideClass(className : STRING);
```

```python
def vs.HideClass(className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
If you're hiding a class for the purpose of printing with that class turned off, you have to do a [ReDrawAll](ReDrawAll.md) before calling the the *[DoMenuTextByName](DoMenuTextByName.md)*('Print',0) call, or else the class doesn't get hidden until after the script completes execution.

## Examples
#### VectorScript ####
```pascal
HideClass('Dimension');
```
#### Python ####
```python
vs.HideClass('Dimension')
```

```pascal
BEGIN
boo := ResourceIsOK;
gClassName := getlocstr(12022, 1);
IF NOT(classexists(gClassName)) THEN goto 99;
if GetCVis(gClassName)=0 then hideclass(gClassName) else showclass(gClassName);
99:END;
RUN(ToggleRLClass);

BEGIN
	FOR i:=1 to ClassNum DO hideclass(classlist(i));
	hlyr:=flayer;
	WHILE (hlyr <> NIL) DO
		BEGIN
			lnm := GetLName(hlyr);

						SetClFillBack (UserClassName, DecimalToColorIndex(TmpClassInfo.FillBack));
						SetClUseGraphic (UserClassName, TmpClassInfo.UseAtCreation);
}
						{set the class visiblity for this class for this sheet}
						IF visibility = 'I' THEN HideClass (UserClassName)
						ELSE IF visibility = 'G' THEN GrayClass (UserClassName)
							ELSE ShowClass (UserClassName);
						IF visibility = 'A' THEN  actClass := UserClassName;
					END
```
```python
elif ( classVis_Curb == -1 ):
	vs.HideClass( gCurb_Class )
```

## See Also
VS Functions:
[ShowClass](ShowClass.md)

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
