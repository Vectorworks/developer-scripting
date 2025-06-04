# SetLBItemInfo

## Description
Sets data for item.

```pascal
FUNCTION SetLBItemInfo(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				itemString   : STRING;
				imageIndex   : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemInfo(dialogID, componentID, itemIndex, subItemIndex, itemString, imageIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the item index|
|subItemIndex|INTEGER|the subitem index|
|itemString|STRING|the item text|
|imageIndex|INTEGER|the item image list index|

## Remarks
The issue represented is the difference between indexing required by this routine (as to VW 12.5.1):

PC needs a 1-based index.
Mac needs a 0-based index.

A commented explanation of this issue has been posted on [http://www.vectorlab.info/index.php?title=List_browser_index_quirks_-_PC_Mac VectorLab], including screenshots of the different results between the two platforms.

## Examples
==== VectorScript ====
```pascal
PROCEDURE testLB_index;
CONST
cLBWidth = 50; { width in characters }
cLBHeight = 22;

kLBControlTypeNone = 1;
kLBDisplayTypeText = 2;

cLB = 10;
cPu_LoadRowsMac = 11;
cPu_LoadRowsPC = 12;

VAR
platform, gD, gDlogResult : INTEGER;
gIsMac : BOOLEAN;

i, n : INTEGER;
temp_r : REAL;
temp_i : INTEGER;
temp_s : STRING;
temp_b : BOOLEAN;


{ ************************************************* }
{ builds up the layout }
FUNCTION Dialog_Layout: INTEGER;
VAR
dialogID : INTEGER;
BEGIN
dialogID := CreateLayout('Test List Browser indexes', True, 'Exit', '');
CreateLB(dialogID, cLB, cLBWidth, cLBHeight);
CreatePushButton(dialogID, cPu_LoadRowsMac, 'Load 5 rows with Mac index');
CreatePushButton(dialogID, cPu_LoadRowsPC, 'Load 5 rows with PC index');

SetFirstLayoutItem(dialogID, cLB);
SetBelowItem(dialogID, cLB, cPu_LoadRowsMac, 0, 0);
SetBelowItem(dialogID, cPu_LoadRowsMac, cPu_LoadRowsPC, 0, 0);

Dialog_Layout := dialogID;
END;


{ ************************************************* }
{ disalog driver }
PROCEDURE Dialog_Events(VAR item:LONGINT; data:LONGINT);
VAR
result : BOOLEAN;
i, n : INTEGER;


{ **************************** set up a 2 columns LB }
PROCEDURE Make2col_LB(listBrowser: LONGINT; colTitle0, colTitle1: STRING; colWidth: INTEGER);
VAR
colNum, rowNum : INTEGER;

BEGIN
colNum := InsertLBColumn(gD, listBrowser, 0, colTitle0, colWidth);
temp_b := SetLBControlType(gD, listBrowser, colNum, kLBControlTypeNone);
temp_b := SetLBItemDisplayType(gD, listBrowser, colNum,	kLBDisplayTypeText);

colNum := InsertLBColumn(gD, listBrowser, 1, colTitle1, colWidth);
temp_b := SetLBControlType(gD, listBrowser, colNum, kLBControlTypeNone);
temp_b := SetLBItemDisplayType(gD, listBrowser, colNum, kLBDisplayTypeText);

EnableLBColumnLines(gD, listBrowser, TRUE);
END;

{ **************************** insert 1 row in a LB }
PROCEDURE InsertRow(d, lb: LONGINT; detract: INTEGER);
VAR
rowIndx, newRowIndx : INTEGER;
BEGIN
rowIndx := GetNumLBItems(d, lb);
newRowIndx := InsertLBItem(d, lb, rowIndx, concat(rowIndx));

newRowIndx := newRowIndx - detract;
{ SetLBItemInfo is 0-based on Mac, 1-based on PC }

temp_b := SetLBItemInfo(d, lb, newRowIndx, 1, concat(newRowIndx), 0);
temp_b := RefreshLB(d, lb);
END;

BEGIN
CASE item OF
SetupDialogC:
BEGIN
Make2col_LB(cLB, 'Row index', 'newRowIndx ', 100);
{ first rows are OK }
temp_i := 0;
IF gIsMac THEN
temp_i := 1;

FOR i := 1 TO 5 DO
InsertRow(gD, cLB, temp_i);
END;

cPu_LoadRowsMac:
FOR i := 1 TO 5 DO
InsertRow(gD, cLB, 1);

cPu_LoadRowsPC:
FOR i := 1 TO 5 DO
InsertRow(gD, cLB, 0);

END; {of item}
END;

{ *********************** MAIN ************************** }

BEGIN
GetVersion(temp_i, temp_i, temp_i, platform);
gIsMac := (platform = 1);

gD := Dialog_Layout;
IF VerifyLayout(gD) THEN
gDlogResult := RunLayoutDialog(gD, Dialog_Events);
END;
Run(testLB_index);
```
Here's an other, shorter example:
```pascal
PROCEDURE Test;
VAR
	id,cnt,tmpint,platform,ExtraRowInd : INTEGER;
	bool : BOOLEAN;

	PROCEDURE DialogHandler(VAR item : LONGINT; data : LONGINT);
	BEGIN
		CASE item OF
			SetupDialogC:
			BEGIN
			{insert 3 columns into the List Browser}
				tmpint:=InsertLBColumn(id,999,0,'column 1',80);
				tmpint:=InsertLBColumn(id,999,1,'column 2',80);
				tmpint:=InsertLBColumn(id,999,2,'column 3',80);
			{fill the columns}
				FOR cnt:=0 TO 3 DO
				BEGIN
				{insert a row and fill in the value in the first column of that row}
					tmpint:=InsertLBItem(id,999,cnt,Num2StrF(cnt));
				{fill in a value in the 2 remaining columns of that row}
					bool:=SetLBItemInfo(id,999,cnt,1-ExtraRowInd,'col2',0);
					bool:=SetLBItemInfo(id,999,cnt,2-ExtraRowInd,'col3',0);
				END;
			END;
		END;
	END;
BEGIN
	GetVersion(tmpint,tmpint,tmpint,platform);
	IF platform = 1 THEN ExtraRowInd:=1 ELSE ExtraRowInd:=0;
	
	id:=CreateLayout('',FALSE,'OK','Cancel');
	CreateLB(id,999,50,20);
	SetFirstLayoutItem(id,999);
	tmpint:=RunLayoutDialog(id,DialogHandler);
END;
RUN(Test);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
