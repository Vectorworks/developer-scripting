# GetClUseGraphic

## Description
Returns whether the graphic attributes of the specified class will be used at object creation.

```pascal
FUNCTION GetClUseGraphic(className : STRING): BOOLEAN;
```

```python
def vs.GetClUseGraphic(className):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
Returns whether the class is set to use its graphic attributes at object creation.

## Examples
```pascal
BEGIN
	SetClass (pluginH, userClassName);
	IF GetClUseGraphic (userClassName) THEN SetAttrsByClass (pluginH);
END;

						IF GetClUseGraphic  (UserClassName) <> TmpClassInfo.UseAtCreation THEN
							SetClUseGraphic (UserClassName, TmpClassInfo.UseAtCreation);
{
						SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));
						SetClLW (UserClassName, TmpClassInfo.LW);
						SetClLSN (UserClassName, TmpClassInfo.LS);

IF GetClUseGraphic (UserClassName) <> TmpClassInfo.UseAtCreation THEN
BEGIN
	IF GetClUseGraphic  (UserClassName) THEN
	BEGIN
		gClassList [classIndex].UseAtCreation := TRUE;
		WriteToClassWS (classIndex, 7, 1, '');
	END
```
```python
if vs.GetTypeN( vs.GetObject( userClassName ) ) == 94:
	vs.SetClass( pluginH, userClassName )
	if vs.GetClUseGraphic( userClassName ):
		SetAttrsByClass( pluginH )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
