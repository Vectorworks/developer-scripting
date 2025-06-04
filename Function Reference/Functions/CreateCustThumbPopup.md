# CreateCustThumbPopup

## Description
Creates a custom thumbnail popup that can be populated with previews of objects in Vectorworks.

```pascal
PROCEDURE CreateCustThumbPopup(
				dialogID  : LONGINT;
				controlID : LONGINT;
				sizeType  : INTEGER);
```

```python
def vs.CreateCustThumbPopup(dialogID, controlID, sizeType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by the command to create the dialog.|
|controlID|LONGINT|The identifier that should be assigned to the control.|
|sizeType|INTEGER|The size type of the control|

## Remarks
There are two thumbnail sizes at the moment, 64x64 and 128x32.
* sizeType = 0
** The default size (64x64) used for most of the resource types.
* sizeType = 1
** The LineType size (128x32) used for displaying Line Types..

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
