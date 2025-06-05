# AddLBImage

## Description
_[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md) DEPRECATED after Vectorworks2012_. See [AddListBrowserImage](AddListBrowserImage.md) for a replacement.

Adds specified image resource to image list.

Currently only one resource type is supported: the 'ics8' resource.  This is a 16x16 color icon.  Pass a value of 1 for the resourceType argument to indicate this type.  Call SetVSResourceFile to specify a resource file that contains the icons.

```pascal
FUNCTION AddLBImage(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				resourceType : INTEGER;
				resourceID   : INTEGER): INTEGER;
```

```python
def vs.AddLBImage(dialogID, componentID, resourceType, resourceID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|resourceType|INTEGER|type of image resource to be added|
|resourceID|INTEGER|the resource ID of image to add|

## Remarks
The index returned is 0-based.

## Examples
Here's an annoying example of how to use icons in LB and get their status:
```pascal
PROCEDURE Test;
CONST
	kLB = 10;
VAR
	dialogID, int1, cnt, platform, macSubtract : INTEGER;
	bool : BOOLEAN;
	LBicon1, LBicon2 : INTEGER;
	LBiconCheck : INTEGER;
	LBiconUnCheck : INTEGER;
	tmpStr : STRING;
	
	PROCEDURE DialogHandler(VAR item : LONGINT; data : LONGINT);
	BEGIN
		CASE item OF
		SetupDialogC:
			BEGIN
				{ add some images to the image list }
				LBicon1 := AddLBImage(dialogID, kLB, 1, 11022);	{ 11022 = check mark icon }
				LBicon2 := AddLBImage(dialogID, kLB, 1, 11023);	{ 11023 = blank icon }

				{ insert the first column into the List Browser }
				int1 := InsertLBColumn(dialogID, kLB, 0, 'col 1', 60);

				{ insert the second column into the List Browser }
				int1 := InsertLBColumn(dialogID, kLB, 1, 'col 2', 80);

				{ set the control type of the columns, column1: multi state, column2: static }
				bool := SetLBControlType(dialogID, kLB, 0, 3);
				bool := SetLBControlType(dialogID, kLB, 1, 1);

				{ set the display type of the columns, column1: icon only, column2: text only }
				bool := SetLBItemDisplayType(dialogID, kLB, 0, 1);
				bool := SetLBItemDisplayType(dialogID, kLB, 1, 0);

				{ insert the icons into the first column so it can be used }
				LBiconCheck := InsertLBColumnDataItem(dialogID, kLB, 0, 'on', LBicon1, -1, 0);
				LBiconUnCheck := InsertLBColumnDataItem(dialogID, kLB, 0, 'off', LBicon2, -1, 0);

				{ fill the columns }
				FOR cnt:=0 TO 3 DO BEGIN
					int1 := InsertLBItem(dialogID, kLB, cnt, '');
					bool := SetLBItemInfo(dialogID, kLB, cnt, 1, Num2Str(0, cnt) ,0);
				END;
			END;

		kLB:	{ if the user has clicked in the LB }
			BEGIN
				{ loop trough the rows }
				FOR cnt := 0 TO 3 DO BEGIN
					{ get the information of the first cel of the row }
					bool := GetLBItemInfo(dialogID, kLB, cnt, 0, tmpStr, int1);
					
					{ if the cell is checked... }
					IF (int1 = LBiconCheck) THEN 
						AlrtDialog(Concat('You checked row ', Num2Str(0, cnt+1), '.'));
				END;
			END;
		END; { case }
	END;

BEGIN
	{ we're going to use an icon out of the file "IP Resources", so let VW check first if this one is located in the Plug-Ins folder }
	
	IF SetVSResourceFile('IP Resources') THEN BEGIN
		{ create the Dialoglayout and put a ListBrowser in the dialog }
		dialogID := CreateLayout('', FALSE, 'OK', 'Cancel');
		CreateLB(dialogID, kLB, 50, 20);
		SetFirstLayoutItem(dialogID, kLB);
		
		{ run the dialog }
		int1 := RunLayoutDialog(dialogID, DialogHandler);
	END;
END;
RUN(Test);
```
#### Python ####
```python
def DialogHandler(item, data):
	if(item ==  SetupDialogC):
		#{ add some images to the image list }
		LBicon1 = vs.AddLBImage(dialogID, kLB, 1, 11022)	#{ 11022 = check mark icon }
		LBicon2 = vs.AddLBImage(dialogID, kLB, 1, 11023)	#{ 11023 = blank icon }

		#{ insert the first column into the List Browser }
		int1 = vs.InsertLBColumn(dialogID, kLB, 0, 'col 1', 60)

		#{ insert the second column into the List Browser }
	 int1 = vs.InsertLBColumn(dialogID, kLB, 1, 'col 2', 80)

		#{ set the control type of the columns, column1: multi state, column2: static }
		bool = vs.SetLBControlType(dialogID, kLB, 0, 3)
		bool = vs.SetLBControlType(dialogID, kLB, 1, 1)

		#{ set the display type of the columns, column1: icon only, column2: text only }
		bool = vs.SetLBItemDisplayType(dialogID, kLB, 0, 1)
		bool = vs.SetLBItemDisplayType(dialogID, kLB, 1, 0)

		#{ insert the icons into the first column so it can be used }
		LBiconCheck = vs.InsertLBColumnDataItem(dialogID, kLB, 0, 'on', LBicon1, -1, 0)
		LBiconUnCheck = vs.InsertLBColumnDataItem(dialogID, kLB, 0, 'off', LBicon2, -1, 0)

		#{ fill the columns }
		for cnt in range(0,3):
			int1 = vs.InsertLBItem(dialogID, kLB, cnt, '')
			bool = vs.SetLBItemInfo(dialogID, kLB, cnt, 1, vs.Num2Str(0, cnt) ,0)

	elif(item ==  kLB):
		#{ if the user has clicked in the LB }
		#{ loop trough the rows }
		for cnt in range(0,3):
			#{ get the information of the first cel of the row }
			bool = vs.GetLBItemInfo(dialogID, kLB, cnt, 0, tmpStr, int1);
			#{ if the cell is checked... }
			if (int1 == LBiconCheck): 
				vs.AlrtDialog(vs.Concat('You checked row ', vs.Num2Str(0, cnt+1), '.'));

def Test():
	global kLB, SetupDialogC, dialogID
	kLB = 10
	SetupDialogC = 12255
	#{ we're going to use an icon out of the file "IP Resources", so let VW check first if this one is located in the Plug-Ins folder }
	if vs.SetVSResourceFile('IP Resources'):
		#{ create the Dialoglayout and put a ListBrowser in the dialog }
		dialogID = vs.CreateLayout('', 0, 'OK', 'Cancel')
		vs.CreateLB(dialogID, kLB, 50, 20)
		vs.SetFirstLayoutItem(dialogID, kLB)
		
		#{ run the dialog }
		int1 = vs.RunLayoutDialog(dialogID, DialogHandler)
Test()
```

## See Also
VS Functions:
[SetVSResourceFile](SetVSResourceFile.md) 
| [CreateLB](CreateLB.md) 
| [InsertLBColumn](InsertLBColumn.md) 
| [SetLBControlType](SetLBControlType.md) 
| [SetLBItemDisplayType](SetLBItemDisplayType.md) 
| [InsertLBColumnDataItem](InsertLBColumnDataItem.md) 
| [SetLBItemUsingColumnDataItem](SetLBItemUsingColumnDataItem.md) 
| [InsertLBItem](InsertLBItem.md) 
| [EnableLBColumnLines](EnableLBColumnLines.md)

## Version
Availability: from VectorWorks 11.0
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
