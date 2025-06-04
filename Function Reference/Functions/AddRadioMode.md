# AddRadioMode

## Description
Adds a group of buttons with an image to the mode bar for a tool. Replaces vstAddRadioMode

```pascal
PROCEDURE AddRadioMode(
				initialSetting  : INTEGER;
				buttonCount     : INTEGER;
				imageSpecifier1 : DYNARRAY[] of CHAR;
				imageSpecifier2 : DYNARRAY[] of CHAR;
				imageSpecifier3 : DYNARRAY[] of CHAR;
				imageSpecifier4 : DYNARRAY[] of CHAR;
				imageSpecifier5 : DYNARRAY[] of CHAR;
				imageSpecifier  : DYNARRAY[] of CHAR);
```

```python
def vs.AddRadioMode(initialSetting, buttonCount, imageSpecifier1, imageSpecifier2, imageSpecifier3, imageSpecifier4, imageSpecifier5, imageSpecifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|initialSetting|INTEGER|   |
|buttonCount|INTEGER|   |
|imageSpecifier1|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier2|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier3|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier4|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier5|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
