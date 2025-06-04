# CreateThumbnailPopup

## Description
Creates a thumbnail popup that can be populated with previews of objects in Vectorworks.

```pascal
PROCEDURE CreateThumbnailPopup(
				dialogID  : LONGINT;
				controlID : LONGINT);
```

```python
def vs.CreateThumbnailPopup(dialogID, controlID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|controlID|LONGINT|   |

## Remarks
'''BE AWARE:''' this will not work for Line Types of an external document (default library for example). Use [[VS:CreateCustThumbPopup]] in that situation.

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
