# SetLayoutDialogPosition

## Description
This function moves the dialog window to the given location.  Call this function to override the default automatic positioning of the dialog window.  The dialog will be pinned so that it is at least partly onscreen.

This function can be useful for displaying a dialog in a position in which it was placed during prior use.

```pascal
FUNCTION SetLayoutDialogPosition(
				dialogID : LONGINT;
				left     : INTEGER;
				top      : INTEGER): BOOLEAN;
```

```python
def vs.SetLayoutDialogPosition(dialogID, left, top):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index of the dialog.|
|left|INTEGER|Location of left edge of dialog in pixels.|
|top|INTEGER|Location of top edge of dialog in pixels.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Dialog;
VAR
   id,tmpInt : INTEGER;
   result : BOOLEAN;

   PROCEDURE dialog_Handler(VAR item : LONGINT; data : LONGINT);
   BEGIN
      CASE item OF
         SetupDialogC:
         BEGIN
            result:=SetLayoutDialogPosition(id,100,100);
         END;
         1: ;
         2: ;
      END;
   END;
   
BEGIN
   id:=CreateLayout('Title',FALSE,'OK','Cancel');
   CreateStaticText(id,100,'Message',20);
   SetFirstLayoutItem(id,100);
   tmpInt:=RunLayoutDialog(id,dialog_Handler);
END;
RUN(Dialog);
```
==== Python ====
```python

```

## See Also
VS Functions:
[GetLayoutDialogPosition](GetLayoutDialogPosition.md)

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
