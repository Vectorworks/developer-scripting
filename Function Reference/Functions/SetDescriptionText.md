# SetDescriptionText

## Description
Sets the user-supplied description for an object.<BR>
Adds the description data node if one does not already exist.

```pascal
FUNCTION SetDescriptionText(
				hObject         : HANDLE;
				descriptionText : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.SetDescriptionText(hObject, descriptionText):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle of the object for which the description should be set.|
|descriptionText|DYNARRAY[] of CHAR|The description text to be set for the object|

## Remarks
Added for T01363 to add descriptions for classes and layers.

## Examples
```pascal
BEGIN
	GetWSCellString (wksHand, row, col+8, tempStr);	{description}
	tempBool := SetDescriptionText (classHand, tempStr);
END;

BEGIN
	descriptionTextDyn := descriptionTextStr;
	tempBool := SetDescriptionText (sheetLayerH, descriptionTextDyn);
END;

GetDescriptionText (classHandle, tempDescTextDyn);
tempDescTextStr := tempDescTextDyn;
IF tempDescTextStr <> gClassList [i].Description THEN
	tempBool := SetDescriptionText (classHandle, gClassList [i].Description);
```
```python
import vs

# Sets the user-supplied description for an object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
descriptionText = 'Example text'

ok = vs.SetDescriptionText(hObject, descriptionText)
if ok:
    vs.Message('SetDescriptionText succeeded')
else:
    vs.Message('SetDescriptionText failed')
```

## See Also
VS Functions:
[GetDescriptionText](GetDescriptionText.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
