# VerifyLayout

## Description
Checks a specified dialog layout for correct layout definition.

```pascal
FUNCTION VerifyLayout(dialogID : LONGINT): BOOLEAN;
```

```python
def vs.VerifyLayout(dialogID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout to be verified.|

## Remarks
[DWD 1/20/00]

## Examples
#### VectorScript ####
```pascal
{verify the dialog layou is properly constructed}
dialogOK := VerifyLayout(lEditID);

IF (dialogOK &amp; rsAvailable) THEN
BEGIN
lmtestResult := RunLayoutDialog(lEditID,DriveSplashDialog);
END;
```
#### Python ####
```python

```

```pascal
dialogID := define_MainDialog;
dialogOK := VerifyLayout (dialogID);
exitState := RunNamedDialog (dialogID, getInfo_Main, 'ArcBySegLength');

BEGIN
	dialogID := defineDialog_Main;
	dialogOK := VerifyLayout (dialogID);
	exitState := RunNamedDialog (dialogID, displayDialog, 'ArcIntoSegments');

dialogID := defineDialog_Main;
dialogOK := VerifyLayout (dialogID);
```
```python
result = vs.VerifyLayout(dialogID)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
