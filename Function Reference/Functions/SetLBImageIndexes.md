# SetLBImageIndexes

## Description
Sets the images for the list browser row, Replaces SetLBMultImageIndexes

```pascal
FUNCTION SetLBImageIndexes(
				dialogID        : LONGINT;
				controlID       : LONGINT;
				itemIndex       : INTEGER;
				subItemIndex    : INTEGER;
				imageSpecifier0 : DYNARRAY[] of CHAR;
				imageSpecifier1 : DYNARRAY[] of CHAR;
				imageSpecifier2 : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.SetLBImageIndexes(dialogID, controlID, itemIndex, subItemIndex, imageSpecifier0, imageSpecifier1, imageSpecifier2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by the command to create the dialog.|
|controlID|LONGINT|The identifier of the control to be updated.|
|itemIndex|INTEGER|   |
|subItemIndex|INTEGER|   |
|imageSpecifier0|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier1|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier2|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Examples
```pascal
resultOK := SetLBImageIndexes(1, 2, 3, 10, imageSpecifier0, imageSpecifier1, imageSpecifier2);
```
```python
import vs

# Sets the images for the list browser row, Replaces SetLBMultImageIndexes.
dialogID = 1
controlID = 2
itemIndex = 1
subItemIndex = 1
imageSpecifier0 = 'Example'
imageSpecifier1 = 'Example'
imageSpecifier2 = 'Example'

ok = vs.SetLBImageIndexes(dialogID, controlID, itemIndex, subItemIndex, imageSpecifier0, imageSpecifier1, imageSpecifier2)
if ok:
    vs.Message('SetLBImageIndexes succeeded')
else:
    vs.Message('SetLBImageIndexes failed')
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
