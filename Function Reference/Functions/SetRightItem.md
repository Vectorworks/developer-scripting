# SetRightItem

## Description
Places the specified control item to the right of a previously inserted control item.
Additional positioning can be performed by specifying x- and y-offsets (in pixels) from the initial insert position.

```pascal
PROCEDURE SetRightItem(
				dialogID    : LONGINT;
				srcItemID   : LONGINT;
				rightItemID : LONGINT;
				indent      : INTEGER;
				lineSpacing : INTEGER);
```

```python
def vs.SetRightItem(dialogID, srcItemID, rightItemID, indent, lineSpacing):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout being defined.|
|srcItemID|LONGINT|The index of the anchor control item.|
|rightItemID|LONGINT|The index of the control item being placed.|
|indent|INTEGER|Left-right (x) control offset value.|
|lineSpacing|INTEGER|Up-down (y) control offset value.|

## Remarks
Use the indent and lineSpacing sparingly.[DWD 1/20/00]

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
