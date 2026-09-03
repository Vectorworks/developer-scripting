# SetClUseGraphic

## Description
Toggles the document setting for using the graphic attributes of the specified class at object creation.

```pascal
PROCEDURE SetClUseGraphic(
				className : STRING;
				use       : BOOLEAN);
```

```python
def vs.SetClUseGraphic(className, use):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|use|BOOLEAN|Use graphic attributes on-off setting.|

## Remarks
Sets whether the class graphic attributes are used at object creation.

## Examples
#### VectorScript ####
```pascal
SetClUseGraphic('Forested Cover',TRUE);
```
#### Python ####
```python

```

```pascal
		END
		{Cannot create class _____; an object of type ____ with that name already exists.}
end else BEGIN
	NameClass(className);
	SetClUseGraphic(className, TRUE);
	SetClUseTexture(className, TRUE);
END;

GetWSCellString (wksHand, row, col+7, tempStr);	{use at creation}
SetClUseGraphic (userClassName, Str2Boo(tempStr));

						IF GetClUseGraphic  (UserClassName) <> TmpClassInfo.UseAtCreation THEN
							SetClUseGraphic (UserClassName, TmpClassInfo.UseAtCreation);
{
						SetClPenFore (UserClassName, DecimalToColorIndex(TmpClassInfo.PenColor));
						SetClLW (UserClassName, TmpClassInfo.LW);
						SetClLSN (UserClassName, TmpClassInfo.LS);
```
```python
else:
	# Cannot create class _____; an object of type ____ with that name already exists.
	vs.NameClass( className )
	vs.SetClUseGraphic( className, True )
	vs.SetClUseTexture( className, True )

vs.SetClFillBack( userClassName, r, g, b )
tempStr = vs.GetWSCellString( wksHand, row, col + 7 )
# use at creation
vs.SetClUseGraphic( userClassName, Common.Includes.Utilities_General.Str2Boo( tempStr ) )
```
See also in tutorials: [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
