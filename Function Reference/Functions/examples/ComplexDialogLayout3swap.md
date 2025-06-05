## VectorScript example

```pascal
PROCEDURE dialog1_Main;
CONST
  kOK            = 1;
  kCancel        = 2;
  kSwapControl   = 4;
  kSwapPane_1    = 5;
  kSwapPane_2    = 6;
  kButton_1      = 13;
  kButton_2      = 15;
VAR
  dialog1          :INTEGER;

PROCEDURE dialog1_Setup;
BEGIN
  dialog1 := CreateLayout('Swap control', FALSE, 'OK', 'Cancel');
  CreateSwapControl        (dialog1, kSwapControl);
  CreateGroupBox           (dialog1, kSwapPane_1,    'Swap Pane 1', TRUE);
  CreateGroupBox           (dialog1, kSwapPane_2,    'Swap Pane 2', TRUE);
  CreatePushButton         (dialog1, kButton_1,      'Go to second pane...');
  CreatePushButton         (dialog1, kButton_2,      '... go to first pane');
  
  SetFirstLayoutItem(dialog1, kSwapControl);
  
  CreateSwapPane    (dialog1, kSwapControl,    kSwapPane_1);
  SetFirstGroupItem (dialog1, kSwapPane_1,     kButton_1);

  CreateTabPane     (dialog1, kSwapControl,    kSwapPane_2);
  SetFirstGroupItem (dialog1, kSwapPane_2,     kButton_2);
END;

PROCEDURE dialog1_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
  CASE item OF
  kButton_1: BEGIN
      DisplaySwapPane(dialog1, kSwapControl, 2);
    END;
  kButton_2: BEGIN
      DisplaySwapPane(dialog1, kSwapControl, 1);
    END;
  END;
END;

BEGIN
  dialog1_Setup;
  IF RunLayoutDialog(dialog1, dialog1_Handler) = 1 THEN BEGIN
    END;
END;
RUN(dialog1_Main);
```

## Python example

```python
kOK            = 1
kCancel        = 2
kSwapControl   = 4
kSwapPane_1    = 5
kSwapPane_2    = 6
kButton_1      = 13
kButton_2      = 15

dialog1 = 0

def dialog1_Setup():
  global dialog1
  dialog1 = vs.CreateLayout('Swap control', False, 'OK', 'Cancel')
  vs.CreateSwapControl        (dialog1, kSwapControl)
  vs.CreateGroupBox           (dialog1, kSwapPane_1,    'Swap Pane 1', True)
  vs.CreateGroupBox           (dialog1, kSwapPane_2,    'Swap Pane 2', True)
  vs.CreatePushButton         (dialog1, kButton_1,      'Go to second pane...')
  vs.CreatePushButton         (dialog1, kButton_2,      '... go to first pane')
  
  vs.SetFirstLayoutItem(dialog1, kSwapControl)
  
  vs.CreateSwapPane    (dialog1, kSwapControl,    kSwapPane_1)
  vs.SetFirstGroupItem (dialog1, kSwapPane_1,     kButton_1)

  vs.CreateTabPane     (dialog1, kSwapControl,    kSwapPane_2)
  vs.SetFirstGroupItem (dialog1, kSwapPane_2,     kButton_2)

def dialog1_Handler(item,data):
  if item == kButton_1:
      vs.DisplaySwapPane(dialog1, kSwapControl, 2)
  elif item == kButton_2:
      vs.DisplaySwapPane(dialog1, kSwapControl, 1)

dialog1_Setup()
if vs.RunLayoutDialog(dialog1, dialog1_Handler) == 1:
    pass
```
