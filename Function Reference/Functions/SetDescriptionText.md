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

## See Also
VS Functions:
[GetDescriptionText](GetDescriptionText.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
