# SetEditReal

## Description
Sets the numeric value of the specified REAL numeric edit field control.

**Table - Field Types for EditReal Fields**

| Index | Field Value   |
|-------|--------------|
| 1     | REAL value   |
| 2     | Angular value|
| 3     | Dimension    |
| 4     | X coordinate |
| 5     | Y coordinate |

```pascal
PROCEDURE SetEditReal(
				dialogID     : LONGINT;
				itemID       : LONGINT;
				editRealType : LONGINT;
				value        : REAL);
```

```python
def vs.SetEditReal(dialogID, itemID, editRealType, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the control item.|
|editRealType|LONGINT|The type of REAL value displayed in the field.|
|value|REAL|The new value for the field.|

## Remarks
Note that dimension reals do not accept negative numbers. If your field might contain negatives, and you still want the units mark to show, use x or y coordinate reals.

## Examples
```pascal
numCols := p__numCols;
gridFreq := p__gridFreq;
SetEditInteger (dlogID,8,numRows);
SetEditInteger (dlogID,9,numCols);
SetEditReal (dlogID,10,3,gridFreq);
SelectEditText(dlogID, 8);

	SetLineTypeAttriData(IDLabelDialog,kBubbleLS,BubbleLS,BubbleLW);
	SetBooleanItem(IDLabelDialog, kShowLeader,DWShowLeader);
	SetBooleanItem(IDLabelDialog, kUseMarker,UseMarker);
	SetBooleanItem(IDLabelDialog, kAutoRotate,DWHorz);
	SetEditReal(IDLabelDialog, kBubbleSize, 3, DWBubbleSize);
	SetMarkerValue( IDLabelDialog, kLeaderStyle, DWMarkerStyle, MarkerAngle, MarkerSize, MarkerWidth, MarkerBasis, MarkerThickness );
	SetItemText(IDLabelDialog, kFieldValue,gDataArr[1,2]);
	SetItemText(IDLabelDialog, kFieldName,gDataArr[1,1]);
END;

	SetSelChoice(dlgId,  kClassPopup, strClassTemp); {from Utilities_Dialogs.px}
	{SelectChoice( dlgId,  kClassPopup, 1, TRUE);}
	SetEditReal( dlgId, kElevationEdit, 3, dElevationTemp );
	SetEditReal( dlgId, kFloorHeightEdit, 3, dThicknessTemp );
END;
```
```python
import vs

# Sets the numeric value of the specified REAL numeric edit field control.
dialogID = 1
itemID = 2
editRealType = 0
value = 1.0

vs.SetEditReal(dialogID, itemID, editRealType, value)
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
