## VectorScript

```pascal
PROCEDURE SampleDlg2;
CONST
    {Alignment constants}
    kRight                = 1;
    kBottom               = 2;
    kLeft                 = 3;
    kColumn               = 4;
    kResize               = 0;
    kShift                = 1;

    { default and cancel button IDs}
    kOK                   = 1;
    kCancel               = 2;

    { control IDs}
    kListBoxText          = 4;
    kListBox1             = 5;
    kListBrowserText      = 6;
    kListBrowser          = 7;
    kListBox2             = 8;

VAR
    dialog            :INTEGER;
    cnt               :INTEGER;

FUNCTION GetPlugInString(ndx :INTEGER) :STRING;
BEGIN
    {Static Text}
    IF ndx = 1001 THEN			GetPlugInString := 'OK'
    ELSE IF ndx = 1002 THEN		GetPlugInString := 'Cancel'
    ELSE IF ndx = 1003 THEN		GetPlugInString := 'Sample Dialog 2'
    ELSE IF ndx = 1004 THEN		GetPlugInString := 'List Box'
    ELSE IF ndx = 1005 THEN		GetPlugInString := ''
    ELSE IF ndx = 1006 THEN		GetPlugInString := 'List Browser'
    ELSE IF ndx = 1007 THEN		GetPlugInString := ''
    ELSE IF ndx = 1008 THEN		GetPlugInString := ''
    ; {Help Text}
    IF ndx = 2001 THEN			GetPlugInString := 'Accepts the dialog data.'
    ELSE IF ndx = 2002 THEN		GetPlugInString := 'Cancels the dialog data.'
    ELSE IF ndx = 2004 THEN		GetPlugInString := ''
    ELSE IF ndx = 2005 THEN		GetPlugInString := 'This is list box control.'
    ELSE IF ndx = 2006 THEN		GetPlugInString := ''
    ELSE IF ndx = 2007 THEN		GetPlugInString := 'This is list browser control.'
    ELSE IF ndx = 2008 THEN		GetPlugInString := 'Tabbed content list box. This list box contains rows with two strings with tab delimiter. This causes the list to have two columns.'
;END;
FUNCTION GetStr(ndx :INTEGER) :STRING;
BEGIN
    GetStr := GetPluginString( ndx + 1000 )
END;

FUNCTION GetHelpStr(ndx :INTEGER) :STRING;
BEGIN
    GetHelpStr := GetPluginString( ndx + 2000 )
END;

BEGIN
    dialog := CreateResizableLayout(GetStr(3), TRUE, GetStr(kOK), GetStr(kCancel), TRUE, TRUE );

    {create controls}
    CreateStaticText( dialog, kListBoxText, GetStr(kListBoxText), -1 );
    CreateListBox( dialog, kListBox1, 25, 10 );
    CreateListBox( dialog, kListBox2, 25, 10 );
    CreateStaticText( dialog, kListBrowserText, GetStr(kListBrowserText), -1 );
    CreateLB( dialog, kListBrowser, 50, 10 );

    {set relations}
    SetFirstLayoutItem( dialog, kListBoxText );
    SetBelowItem( dialog, kListBoxText, kListBox1, 0, 0 );
    SetRightItem( dialog, kListBox1, kListBox2, 0, 0 );
    SetBelowItem( dialog, kListBox1, kListBrowserText, 0, 0 );
    SetBelowItem( dialog, kListBrowserText, kListBrowser, 0, 0 );

    {set alignments}
    AlignItemEdge( dialog, kListBrowser, kRight, 1, kResize );
    AlignItemEdge( dialog, kListBox2, kRight, 1, kResize );

    {set bindings}
    SetEdgeBinding        ( dialog, kListBox1, TRUE, TRUE, FALSE, FALSE );
    SetProportionalBinding( dialog, kListBox1, FALSE, TRUE, FALSE, FALSE );
    SetEdgeBinding        ( dialog, kListBox2, TRUE, TRUE, FALSE, FALSE );
    SetProportionalBinding( dialog, kListBox2, TRUE, FALSE, FALSE, FALSE );

    {set help strings}
    FOR cnt := 1 TO 8 DO SetHelpText(dialog, cnt, GetHelpStr(cnt));
    

    
    IF RunLayoutDialog( dialog, NIL ) = 1 then BEGIN
    END;

END;
RUN( SampleDlg2 );
```

## Python

```python
def MyGetPlugInString(ndx):
    # {Static Text}
    GetPlugInString = ''
    if   ndx == 1001:
        GetPlugInString = 'OK'
    elif ndx == 1002:		
        GetPlugInString = 'Cancel'
    elif ndx == 1003:
        GetPlugInString = 'Sample Dialog 2'
    elif ndx == 1004:
        GetPlugInString = 'List Box'
    elif ndx == 1005: 
        GetPlugInString = ''
    elif ndx == 1006:
        GetPlugInString = 'List Browser'
    elif ndx == 1007:
        GetPlugInString = ''
    elif ndx == 1008:
        GetPlugInString = ''
    # {Help Text}
    if   ndx == 2001:
        GetPlugInString = 'Accepts the dialog data.'
    elif ndx == 2002: 
        GetPlugInString = 'Cancels the dialog data.'
    elif ndx == 2004: 
        GetPlugInString = ''
    elif ndx == 2005:
        GetPlugInString = 'This is list box control.'
    elif ndx == 2006: 
        GetPlugInString = ''
    elif ndx == 2007:
        GetPlugInString = 'This is list browser control.'
    elif ndx == 2008:
        GetPlugInString = 'Tabbed content list box. This list box contains rows with two strings with tab delimiter. This causes the list to have two columns.'
    return GetPlugInString

def GetStr(ndx):
    return MyGetPlugInString( ndx + 1000 )

def GetHelpStr(ndx):
    return MyGetPlugInString( ndx + 2000 )

def SampleDlg2():
    # {Alignment constants}
    kRight                = 1
    kBottom               = 2
    kLeft                 = 3
    kColumn               = 4
    kResize               = 0
    kShift                = 1

    # { default and cancel button IDs}
    kOK                   = 1
    kCancel               = 2

    # { control IDs}
    kListBoxText          = 4
    kListBox1             = 5
    kListBrowserText      = 6
    kListBrowser          = 7
    kListBox2             = 8

    dialog = vs.CreateResizableLayout(GetStr(3), True, GetStr(kOK), GetStr(kCancel), True, True )

    # {create controls}
    vs.CreateStaticText( dialog, kListBoxText, GetStr(kListBoxText), -1 )
    vs.CreateListBox( dialog, kListBox1, 25, 10 )
    vs.CreateListBox( dialog, kListBox2, 25, 10 )
    vs.CreateStaticText( dialog, kListBrowserText, GetStr(kListBrowserText), -1 )
    vs.CreateLB( dialog, kListBrowser, 50, 10 )

    # {set relations}
    vs.SetFirstLayoutItem( dialog, kListBoxText )
    vs.SetBelowItem( dialog, kListBoxText, kListBox1, 0, 0 )
    vs.SetRightItem( dialog, kListBox1, kListBox2, 0, 0 )
    vs.SetBelowItem( dialog, kListBox1, kListBrowserText, 0, 0 )
    vs.SetBelowItem( dialog, kListBrowserText, kListBrowser, 0, 0 )

    # {set alignments}
    vs.AlignItemEdge( dialog, kListBrowser, kRight, 1, kResize )
    vs.AlignItemEdge( dialog, kListBox2, kRight, 1, kResize )

    # {set bindings}
    vs.SetEdgeBinding        ( dialog, kListBox1, True, True, False, False )
    vs.SetProportionalBinding( dialog, kListBox1, False, True, False, False )
    vs.SetEdgeBinding        ( dialog, kListBox2, True, True, False, False )
    vs.SetProportionalBinding( dialog, kListBox2, True, False, False, False )

    # {set help strings}
    for cnt in range(1,8):
        vs.SetHelpText(dialog, cnt, GetHelpStr(cnt))

    if vs.RunLayoutDialog( dialog, None ) == 1:
        pass

SampleDlg2()
```
