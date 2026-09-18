## VectorScript

```pascal
PROCEDURE RUN_InsertSearchableDialog;
CONST
    kOK                   = 1;
    kCancel               = 2;
    kSearchablePulldown   = 4;
VAR
dialog :INTEGER;
result :BOOLEAN;

PROCEDURE InitializeDialog;
VAR res: BOOLEAN;
BEGIN
    res := InsertPulldownSearch(dialog, kSearchablePulldown, 'Test1', 'Test Item #1', 'Item 1 tooltip', '', TRUE);
    res := InsertPulldownSearch(dialog, kSearchablePulldown, 'Test2', 'Test Item #2', 'Item 2 tooltip', '', TRUE);
    res := InsertPulldownSearch(dialog, kSearchablePulldown, 'Test3', 'Test Item #3', 'Item 3 tooltip', '', TRUE);
END;

PROCEDURE dialog_Handler(VAR item :LONGINT; data :LONGINT);
VAR res: BOOLEAN; choice: STRING; selIndex: INTEGER;
BEGIN
   CASE item OF   

      SetupDialogC: BEGIN
	        InitializeDialog;
      END;
         
      kOK: BEGIN
	      GetSelectedChoiceInfo(dialog, kSearchablePulldown, 0, selIndex, choice);
	      AlrtDialog(Concat(choice, ' was selected at index ', selIndex));
      END;

   END;
END;

BEGIN

    {create dialog and controls}
    dialog := CreateLayout('Insert Item', TRUE, 'OK', 'Cancel');

    CreatePulldownSearch( dialog, kSearchablePulldown, 32 );

    {set layout}
    SetFirstLayoutItem( dialog, kSearchablePulldown );

    {run test dialog}
    IF RunLayoutDialog( dialog, dialog_Handler ) = 1 then BEGIN
    END;
END;
RUN(RUN_InsertSearchableDialog);

```
