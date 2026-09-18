# GetDescriptionText

## Description
Retrieves any description text that exists for a specified object and passes it back in the descriptionText argument. The descriptionText argument will be empty if the object has no description text.

```pascal
PROCEDURE GetDescriptionText(
				hObject             : HANDLE;
				VAR descriptionText : DYNARRAY[] of CHAR);
```

```python
def vs.GetDescriptionText(hObject):
    return descriptionText
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle of object for which to retrieve the text.|
|descriptionText|DYNARRAY[] of CHAR|Object's description text, if any exists.|

## Remarks
Added for T01363 to add descriptions for classes and layers.

## Examples
```pascal
PROCEDURE GetDescExample;
VAR
	descriptionTextDyn	:DYNARRAY [] of CHAR;
	tempH : HANDLE;
BEGIN
	tempH := GetObject ('Dimension');

	GetDescriptionText (tempH, descriptionTextDyn);

	IF descriptionTextDyn <> ''  THEN 
		Message (descriptionTextDyn)
	ELSE
		Message ('no description');
END;
Run (GetDescExample);
```

```pascal
BEGIN
	GetDescriptionText (tempH, descriptionTextDyn);
	descriptionTextStr := descriptionTextDyn;
	IF (descriptionTextStr <> '') & (descriptionTextStr <> TmpClassInfo.Description) THEN
	BEGIN
		WriteToClassWS (classIndex, 8, 0, descriptionTextStr);

GetDescriptionText (classHandle, tempDescTextDyn);
tempDescTextStr := tempDescTextDyn;
IF tempDescTextStr <> gClassList [i].Description THEN
	tempBool := SetDescriptionText (classHandle, gClassList [i].Description);
```
```python
import vs

# Retrieves any description text that exists for a specified object and
# passes it back in the descriptionText argument.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetDescriptionText(hObject)
```

## See Also
VS Functions:
[SetDescriptionText](SetDescriptionText.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
