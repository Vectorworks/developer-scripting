# AddListBrowserImage

## Description
Adds an image to a list browser. Replaces AddLBImage.

```pascal
FUNCTION AddListBrowserImage(
				dialogID       : LONGINT;
				controlID      : LONGINT;
				imageSpecifier : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.AddListBrowserImage(dialogID, controlID, imageSpecifier):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by the command to create the dialog.|
|controlID|LONGINT|The identifier of the control to be updated.|
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Examples
```pascal
         kImageCheck := AddListBrowserImage(dlogID,5,'Vectorworks/Standard Images/Checkmark.png');
kImageBlank := AddListBrowserImage(dlogID,5,'Vectorworks/Standard Images/Blank.png');

      kImageCheck := AddListBrowserImage(dialogID, 5, 'Vectorworks/Standard Images/Checkmark.png');
kImageBlank := AddListBrowserImage(dialogID, 5, 'Vectorworks/Standard Images/Blank.png');

gFieldsLBImg1 := AddListBrowserImage(AddEditLegend, kFieldsLB,'Vectorworks/Standard Images/Checkmark.png');
gFieldsLBImg2 := AddListBrowserImage(AddEditLegend, kFieldsLB,'Vectorworks/Standard Images/Blank.png');
```
```python
import vs

# Adds an image to a list browser.
dialogID = 1
controlID = 2
imageSpecifier = 'Example'

resultN = vs.AddListBrowserImage(dialogID, controlID, imageSpecifier)
vs.Message('AddListBrowserImage returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
