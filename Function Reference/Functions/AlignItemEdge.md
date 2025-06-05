# AlignItemEdge

## Description
Aligns the specified control item with other items having the same edge and alignment id values. To align several control items, call this function once for each item to be aligned using a common alignment id value.

{| class="wikitable_c"
|+ Table - Alignment Options
! Index !! Alignment Edge
|-
| align="center" | 1 
| align="center" | Right 
|-
| align="center" | 2 
| align="center" | Bottom 
|-
| align="center" | 3 
| align="center" | Left 
|-
! Index !! Alignment Mode
|-
| align="center" | 0 
| align="center" | Resize control items
|-
| align="center" | 1 
| align="center" | Shift control items
|}


Right alignment of objects will use the object with the minimum pixel value (=distance from the right) as the alignment baseline. Bottom and left alignment of objects will use the object with the  maximum pixel value as the alignment baseline.

```pascal
PROCEDURE AlignItemEdge(
				dialogID  : LONGINT;
				itemID    : LONGINT;
				whichEdge : LONGINT;
				alignID   : INTEGER;
				alignMode : INTEGER);
```

```python
def vs.AlignItemEdge(dialogID, itemID, whichEdge, alignID, alignMode):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout being defined.|
|itemID|LONGINT|The index of the control item to be aligned.|
|whichEdge|LONGINT|The control edge to be aligned.|
|alignID|INTEGER|An arbitrary number used to identify the items to be aligned together.|
|alignMode|INTEGER|Alignment mode of the operation|

## Remarks
Aligns layout items with the same edge and alignID. whichEdge: 1=right, 2=bottom, 3=left; alignMode: resize=0, shift=1

Right aligned objects are lined up with the object with the minimum pixel value. Bottom and left aligned objects are lined up on the maximum pixel value.[DWD 1/20/00]

## Examples
[ComplexDialogLayout](examples/ComplexDialogLayout.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
