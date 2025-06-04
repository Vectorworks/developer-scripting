# ShowItem

## Description
Sets the visibility of the referenced dialog control.

```pascal
PROCEDURE ShowItem(
				dialogID : LONGINT;
				item     : INTEGER;
				show     : BOOLEAN);
```

```python
def vs.ShowItem(dialogID, item, show):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the currently executing dialog.|
|item|INTEGER|Item ID of dialog control to show or hide.|
|show|BOOLEAN|New visibility state of dialog control.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE dialogID_Main;
VAR
dialogID :INTEGER;

PROCEDURE dialogID_Setup;
BEGIN
  dialogID := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
  CreateRadioButton (dialogID,  4,  'Option One');
  CreateEditReal    (dialogID,  5,  1, 0.0, 16);
  CreateRadioButton (dialogID,  6,  'Option Two');
  CreateEditReal    (dialogID,  7,  1, 0.0, 16);
  SetFirstLayoutItem(dialogID,  4);
  SetRightItem      (dialogID,  4,   5,  0, 0);
  SetBelowItem      (dialogID,  4,   6,  0, 0);
  SetRightItem      (dialogID,  6,   7,  0, 0);
END;

PROCEDURE dialogID_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
  SetupDialogC: BEGIN
      ShowItem(dialogID, 4, TRUE);
      ShowItem(dialogID, 7, FALSE);
    END;
  4: BEGIN
      ShowItem(dialogID, 5, TRUE);
      ShowItem(dialogID, 7, FALSE);
    END;
  6: BEGIN
      ShowItem(dialogID, 7, TRUE);
      ShowItem(dialogID, 5, FALSE);
    END;
  END;
END;

BEGIN
  dialogID_Setup;
  IF RunLayoutDialog(dialogID, dialogID_Handler) = 1 THEN BEGIN
  END;
END;
RUN(dialogID_Main);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks11.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
