# IsItemEnabled

## Description
Determines if the specified item is currently enabled.

```pascal
FUNCTION IsItemEnabled(
				nDialogID    : LONGINT;
				nComponentID : LONGINT): BOOLEAN;
```

```python
def vs.IsItemEnabled(nDialogID, nComponentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |

## Examples
```pascal
BEGIN
	IF IsItemEnabled( selectSymbol, kSymsLab ) 	= NOT bMakeAvailable THEN
		EnableItem(selectSymbol, kSymsLab, 	bMakeAvailable);
	IF IsItemEnabled( selectSymbol, kSyms ) 	= NOT bMakeAvailable THEN
		EnableItem(selectSymbol, kSyms, 		bMakeAvailable);
	IF IsItemEnabled( selectSymbol, kOK ) 		= NOT bMakeAvailable THEN
		EnableItem(selectSymbol, kOK,    		bMakeAvailable);

TempS := GetRField( gNumInstRecHand, kNumInstMenu, 'Use1' );
TempB := Str2Boo( TempS );
SetBooleanItem( dialog, kChansCheck1, TempB );
EnableItem( dialog, kIncrEditText1, NOT( TempB ) & IsItemEnabled( dialog, kIncrEditText1 ) );
TempS := GetRField( gNumInstRecHand, kNumInstMenu, 'Use2' );
TempB := Str2Boo( TempS );
SetBooleanItem( dialog, kChansCheck2, TempB );
EnableItem( dialog, kIncrEditText2, NOT( TempB ) & IsItemEnabled( dialog, kIncrEditText2 ) );

EnableItem(dialog, kRRectCrnrRadSizeLab,	(IsItemEnabled(dialog,kBubbleGroupBx))&(AlignChoiceText=GetStr(kBubbleRRect)));
EnableItem(dialog, kRRectCrnrRadSize,		(IsItemEnabled(dialog,kBubbleGroupBx))&(AlignChoiceText=GetStr(kBubbleRRect)));
EnableItem(dialog, kBubbleDetailGrpBx,		(IsItemEnabled(dialog,kBubbleGroupBx))&(tmpBool301));
```
```python
import vs

# Determines if the specified item is currently enabled.
nDialogID = 1
nComponentID = 2

ok = vs.IsItemEnabled(nDialogID, nComponentID)
if ok:
    vs.Message('IsItemEnabled succeeded')
else:
    vs.Message('IsItemEnabled failed')
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
