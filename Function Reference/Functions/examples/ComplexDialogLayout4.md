## VectorScript

```pascal
PROCEDURE LB_LayerList;

VAR
dialog1 : INTEGER;
kImageCheck,kImageBlank,kImageSheet,kImageView : Integer;

{-----------------------------------------------------------------------------}
FUNCTION GetPlugInString(ndx :INTEGER) :STRING;
BEGIN
CASE ndx OF
{Static Text}
3001: GetPlugInString := 'OK';
3002: GetPlugInString := 'Cancel';
3003: GetPlugInString := 'Layers';
END;
END;
{----------------------------------------------------------------------------} 
PROCEDURE Dialog_Setup;
VAR
cnt : INTEGER;
BEGIN
dialog1 := CreateLayout(GetPlugInString(3003),TRUE,GetPlugInString(3001),GetPlugInString(3002));
CreateLB(dialog1,4,25,13);

SetFirstLayoutItem(dialog1,  4);

END;

{-----------------------------------------------------------------------------}

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
Var
ColNum,TempI,I : Integer;
SheetTypeIcon : Integer;
BSB : Boolean;
BSS : String;
LayerHand : Handle;
LayerName,SelectedIconString : String;
SheetIconNumber,SelectedIconNumber : Integer;
BEGIN
CASE item OF
SetupDialogC: 
BEGIN
{These need to be declared as globals otherwise they won't work outside of setup.}
kImageCheck  := AddListBrowserImage(dialog1, 4,'Vectorworks/Standard Images/Checkmark.png');
kImageBlank := AddListBrowserImage(dialog1, 4,'Vectorworks/Standard Images/Blank.png');
kImageSheet := AddListBrowserImage(dialog1, 4,'Vectorworks/Standard Images/SheetLayers.png');
kImageView := AddListBrowserImage(dialog1, 4,'Vectorworks/Standard Images/ViewPage.png');

ColNum := InsertLBColumn(dialog1,4,0,'Use',50);
BSB := SetLBControlType(dialog1,4,ColNum,3);
BSB := SetLBItemDisplayType(dialog1,4,ColNum,1);

{ColNum := InsertLBColumn(dialog1,4,0,'',50);}{This crashes VW}

ColNum := InsertLBColumn(dialog1,4,1,'Layer Name',100);
BSB := SetLBControlType(dialog1,4,ColNum,1);
BSB := SetLBItemDisplayType(dialog1,4,ColNum,3);

ColNum := InsertLBColumnDataItem(dialog1,4,0,'Checked',kImageCheck,-1,0);
ColNum := InsertLBColumnDataItem(dialog1,4,0,'UnChecked',kImageBlank,-1,0);

{Traversing from LLayer by PrevObj doesn't work with Sheet Layers}
LayerHand := FLayer;
I := 0;
While LayerHand <> NIL do
Begin
If GetObjectVariableInt(LayerHand,154) = 2 then
SheetTypeIcon := kImageSheet
else
SheetTypeIcon := kImageView;

ColNum := InsertLBColumnDataItem(dialog1,4,1,GetLName(LayerHand),SheetTypeIcon,SheetTypeIcon,0);

TempI := InsertLBItem (dialog1, 4, I, GetLName(LayerHand));

BSB := SetLBItemUsingColumnDataItem (dialog1, 4, I, 1, ColNum);

BSB := SetLBItemUsingColumnDataItem (dialog1, 4, I, 0, 1);

I := I+1;
LayerHand := NextObj(LayerHand);
End;

EnableLBColumnLines(dialog1,4,True);
END;
1:  BEGIN
For I := 1 to GetNumLBItems(dialog1,4) do 
Begin
BSB := GetLBItemInfo(dialog1,4,I-1,1,LayerName,SheetIconNumber);
BSB := GetLBItemInfo(dialog1,4,I-1,0,SelectedIconString,SelectedIconNumber);
If SheetIconNumber = kImageSheet then
Writeln(LayerName,' is a Sheet Layer and is ',SelectedIconString);

If SheetIconNumber = kImageView then 
Writeln(LayerName,' is a Design Layer and is ',SelectedIconString);
End;
END;

END;
END;
{-----------------------------------------------------------------------------}

BEGIN {Main}
Rewrite('layer.txt');
Dialog_Setup;
IF RunLayoutDialog(dialog1,Dialog_Handler) = 1 THEN 
BEGIN

END;
Close('layer.txt');
END;
Run(LB_LayerList);
```

## Python

```python
def ResourceIsOK():
    _ResourceIsOK = False
    if vs.SetVSResourceFile('IP Resources'):
        _ResourceIsOK = True
    else: 
        vs.Message('The IP Resources file was not found.')
    return _ResourceIsOK

def GetPlugInString(ndx):
    _GetPlugInString = ''
    if ndx == 3001:
        _GetPlugInString = 'OK'
    elif ndx == 3002:
        _GetPlugInString = 'Cancel'
    elif ndx == 3003: 
        _GetPlugInString = 'Layers'
    return _GetPlugInString

def Dialog_Setup():	
    dialog1 = vs.CreateLayout(GetPlugInString(3003),True,GetPlugInString(3001),GetPlugInString(3002))
    vs.CreateLB(dialog1,4,25,13)
    vs.SetFirstLayoutItem(dialog1,  4)
    return dialog1

def Dialog_Handler(item , data ):
    kImageSheet = vs.AddLBImage(dialog1,4,1,11024)
    kImageView = vs.AddLBImage(dialog1,4,1,11025)
    
    if item == SetupDialogC:
        # {These need to be declared as globals otherwise they won't work outside of setup.}
        kImageCheck = vs.AddLBImage(dialog1,4,1,11022)
        kImageBlank = vs.AddLBImage(dialog1,4,1,11023)
        
        ColNum = vs.InsertLBColumn(dialog1,4,0,'Use',50)
        BSB = vs.SetLBControlType(dialog1,4,ColNum,3)
        BSB = vs.SetLBItemDisplayType(dialog1,4,ColNum,1)

        # {ColNum := InsertLBColumn(dialog1,4,0,'',50);}{This crashes VW}

        ColNum = vs.InsertLBColumn(dialog1,4,1,'Layer Name',100)
        BSB = vs.SetLBControlType(dialog1,4,ColNum,1)
        BSB = vs.SetLBItemDisplayType(dialog1,4,ColNum,3)

        ColNum = vs.InsertLBColumnDataItem(dialog1,4,0,'Checked',kImageCheck,-1,0)
        ColNum = vs.InsertLBColumnDataItem(dialog1,4,0,'UnChecked',kImageBlank,-1,0)

        # {Traversing from LLayer by PrevObj doesn't work with Sheet Layers}
        LayerHand = vs.FLayer()
        I = 0
        while LayerHand != None:
            if vs.GetObjectVariableInt(LayerHand,154) == 2:
                SheetTypeIcon = kImageSheet
            else:
                SheetTypeIcon = kImageView
            ColNum = vs.InsertLBColumnDataItem(dialog1,4,1,vs.GetLName(LayerHand),SheetTypeIcon,SheetTypeIcon,0)
            TempI = vs.InsertLBItem (dialog1, 4, I, vs.GetLName(LayerHand))
            BSB = vs.SetLBItemUsingColumnDataItem (dialog1, 4, I, 1, ColNum)
            BSB = vs.SetLBItemUsingColumnDataItem (dialog1, 4, I, 0, 1)
            I = I+1
            LayerHand = vs.NextObj(LayerHand)
        vs.EnableLBColumnLines(dialog1,4,True)
    elif item == 1:
        for I in range(1, vs.GetNumLBItems(dialog1,4)): 
            BSB, LayerName, SheetIconNumber = vs.GetLBItemInfo(dialog1,4,I-1,1)
            BSB, SelectedIconString, SelectedIconNumber = vs.GetLBItemInfo(dialog1,4,I-1,0)
            if SheetIconNumber == kImageSheet:
                vs.Writeln(LayerName,' is a Sheet Layer and is ',SelectedIconString)
            if SheetIconNumber == kImageView: 
                vs.Writeln(LayerName,' is a Design Layer and is ',SelectedIconString)

def LB_LayerList():
    # {-----------------------------------------------------------------------------}
    global dialog1
    vs.Rewrite('layer.txt')
    if ResourceIsOK():
        vs.Message('Hi!')
        dialog1 = Dialog_Setup()
        if vs.RunLayoutDialog(dialog1,Dialog_Handler) == 1:
            pass
        vs.Close('layer.txt')

global SetupDialogC 
dialog1 = 0
SetupDialogC = 12255
LB_LayerList()
```
