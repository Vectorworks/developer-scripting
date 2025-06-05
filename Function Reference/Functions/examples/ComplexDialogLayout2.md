## VectorScript

```pascal
Procedure TestNewControls;
VAR
dlogID, result	: LONGINT;

Procedure DialogProc(VAR item: LONGINT; data: LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
result := 0;
END;

END;
END;

BEGIN
{ ********** CHECK BOX GROUP BOX ********** }

dlogID := CreateLayout('Test New Controls', false, 'OK', 'Cancel');

CreateStaticText(dlogID, 4, 'Check Box Group Box', 20);
SetFirstLayoutItem(dlogID, 4);

{ Check box group box 1 }
CreateCheckBoxGroupBox(dlogID, 5, 'Check Box Group Box 1', TRUE);
SetBelowItem(dlogID, 4, 5, 0, 0);

CreatePushButton(dlogID, 6, 'Alpha');
SetFirstGroupItem(dlogID, 5, 6);

CreatePushButton(dlogID, 7, 'Beta');
SetBelowItem(dlogID, 6, 7, 0, 0);

CreatePushButton(dlogID, 8, 'Gamma');
SetBelowItem(dlogID, 7, 8, 0, 0);

{ Check box group box 2 }
CreateCheckBoxGroupBox(dlogID, 10, 'Check Box Group Box 2', TRUE);
SetRightItem(dlogID, 5, 10, 0, 0);

CreatePushButton(dlogID, 11, 'Ford');
SetFirstGroupItem(dlogID, 10, 11);

CreatePushButton(dlogID, 12, 'Crysler');
SetBelowItem(dlogID, 11, 12, 0, 0);

CreatePushButton(dlogID, 13, 'Honda');
SetBelowItem(dlogID, 12, 13, 0, 0);

{ **********  RADIO BUTTON GROUP BOX ********** }

CreateStaticText(dlogID, 14, 'Radio Button Group Boxes', 25);
SetBelowItem(dlogID, 5, 14, 0, 0);

{ Radio Button Group Box 1 }
CreateRadioButtonGroupBox(dlogID, 15, 'Radio Button Group Box 1', TRUE);
SetBelowItem(dlogID, 14, 15, 0, 0);

CreatePushButton(dlogID, 16, 'Rock');
SetFirstGroupItem(dlogID, 15, 16);

CreatePushButton(dlogID, 17, 'Scissors');
SetBelowItem(dlogID, 16, 17, 0, 0);

CreatePushButton(dlogID, 18, 'Paper');
SetBelowItem(dlogID, 17, 18, 0, 0);

{ Radio Button Group Box 2 }
CreateRadioButtonGroupBox(dlogID, 20, 'Radio Button Group Box 2', TRUE);
SetRightItem(dlogID, 15, 20, 0, 0);

CreatePushButton(dlogID, 21, 'Ebony');
SetFirstGroupItem(dlogID, 20, 21);

CreatePushButton(dlogID, 22, 'Ivory');
SetBelowItem(dlogID, 21, 22, 0, 0);

{ Radio Button Group Box 3 }
CreateRadioButtonGroupBox(dlogID, 25, 'Radio Button Group Box 3', TRUE);
SetRightItem(dlogID, 20, 25, 0, 0);

CreatePushButton(dlogID, 26, 'Engage system');
SetFirstGroupItem(dlogID, 25, 26);

CreateRadioButton(dlogID, 27, 'Warp Engines');
SetBelowItem(dlogID, 26, 27, 0, 0);

CreateRadioButton(dlogID, 28, 'Transporter');	
SetBelowItem(dlogID, 27, 28, 0, 0);

CreateRadioButton(dlogID, 29, 'Photon Torpedos');
SetBelowItem(dlogID, 28, 29, 0, 0);

CreateRadioButton(dlogID, 30, 'Phasers');
SetBelowItem(dlogID, 29, 30, 0, 0);

{ **********  TAB CONTROL ********** }

CreateStaticText(dlogID, 35, 'Tab Control', 15);
SetBelowItem(dlogID, 15, 35, 0, 0);

{ Tab Group 1 }
CreateGroupBox(dlogID, 50, 'Winkin', FALSE);

CreatePushButton(dlogID, 51, 'Button 1');
SetFirstGroupItem(dlogID, 50, 51);

CreatePushButton(dlogID, 52, 'Button 2');
SetBelowItem(dlogID, 51, 52, 0, 0);

CreatePushButton(dlogID, 53, 'Button 3');
SetBelowItem(dlogID, 52, 53, 0, 0);

{ Tab Group 2 }
CreateGroupBox(dlogID, 60, 'Blinkin', FALSE);

CreatePushButton(dlogID, 61, 'Button 1');
SetFirstGroupItem(dlogID, 60, 61);

CreatePushButton(dlogID, 62, 'Button 2');
SetRightItem(dlogID, 61, 62, 0, 0);

CreatePushButton(dlogID, 63, 'Button 3');
SetRightItem(dlogID, 62, 63, 0, 0);

{ Tab Group 3 }
CreateGroupBox(dlogID, 70, 'Nod', FALSE);

CreatePushButton(dlogID, 71, 'Button 1');
SetFirstGroupItem(dlogID, 70, 71);

CreatePushButton(dlogID, 72, 'Button 2');
SetRightItem(dlogID, 71, 72, 0, 0);

CreatePushButton(dlogID, 73, 'Button 3');
SetBelowItem(dlogID, 72, 73, 0, 0);

{ Create tab control }
CreateTabControl(dlogID, 40);
SetBelowItem(dlogID, 35, 40, 0, 0);

{ Add the tab panes }
CreateTabPane(dlogID, 40, 50);
CreateTabPane(dlogID, 40, 60);
CreateTabPane(dlogID, 40, 70);

result := RunLayoutDialog(dlogID, DialogProc);
END;
Run (TestNewControls);
```

## Python

```python
def DialogProc(item, data):
    global SetupDialogC
    SetupDialogC = 12255
    if item == SetupDialogC:
        return 0

def TestNewControls():
    # { ********** CHECK BOX GROUP BOX ********** }
    dlogID = vs.CreateLayout('Test New Controls', False, 'OK', 'Cancel')

    vs.CreateStaticText(dlogID, 4, 'Check Box Group Box', 20)
    vs.SetFirstLayoutItem(dlogID, 4)

    # { Check box group box 1 }
    vs.CreateCheckBoxGroupBox(dlogID, 5, 'Check Box Group Box 1', True)
    vs.SetBelowItem(dlogID, 4, 5, 0, 0)

    vs.CreatePushButton(dlogID, 6, 'Alpha')
    vs.SetFirstGroupItem(dlogID, 5, 6)

    vs.CreatePushButton(dlogID, 7, 'Beta')
    vs.SetBelowItem(dlogID, 6, 7, 0, 0)

    vs.CreatePushButton(dlogID, 8, 'Gamma')
    vs.SetBelowItem(dlogID, 7, 8, 0, 0)

    # { Check box group box 2 }
    vs.CreateCheckBoxGroupBox(dlogID, 10, 'Check Box Group Box 2', True)
    vs.SetRightItem(dlogID, 5, 10, 0, 0)

    vs.CreatePushButton(dlogID, 11, 'Ford')
    vs.SetFirstGroupItem(dlogID, 10, 11)

    vs.CreatePushButton(dlogID, 12, 'Crysler')
    vs.SetBelowItem(dlogID, 11, 12, 0, 0)

    vs.CreatePushButton(dlogID, 13, 'Honda')
    vs.SetBelowItem(dlogID, 12, 13, 0, 0)

    # { **********  RADIO BUTTON GROUP BOX ********** }

    vs.CreateStaticText(dlogID, 14, 'Radio Button Group Boxes', 25)
    vs.SetBelowItem(dlogID, 5, 14, 0, 0)

    # { Radio Button Group Box 1 }
    vs.CreateRadioButtonGroupBox(dlogID, 15, 'Radio Button Group Box 1', True)
    vs.SetBelowItem(dlogID, 14, 15, 0, 0)

    vs.CreatePushButton(dlogID, 16, 'Rock')
    vs.SetFirstGroupItem(dlogID, 15, 16)

    vs.CreatePushButton(dlogID, 17, 'Scissors')
    vs.SetBelowItem(dlogID, 16, 17, 0, 0)

    vs.CreatePushButton(dlogID, 18, 'Paper')
    vs.SetBelowItem(dlogID, 17, 18, 0, 0)

    # { Radio Button Group Box 2 }
    vs.CreateRadioButtonGroupBox(dlogID, 20, 'Radio Button Group Box 2', True)
    vs.SetRightItem(dlogID, 15, 20, 0, 0)

    vs.CreatePushButton(dlogID, 21, 'Ebony')
    vs.SetFirstGroupItem(dlogID, 20, 21)

    vs.CreatePushButton(dlogID, 22, 'Ivory')
    vs.SetBelowItem(dlogID, 21, 22, 0, 0)

    # { Radio Button Group Box 3 }
    vs.CreateRadioButtonGroupBox(dlogID, 25, 'Radio Button Group Box 3', True)
    vs.SetRightItem(dlogID, 20, 25, 0, 0)

    vs.CreatePushButton(dlogID, 26, 'Engage system')
    vs.SetFirstGroupItem(dlogID, 25, 26)

    vs.CreateRadioButton(dlogID, 27, 'Warp Engines')
    vs.SetBelowItem(dlogID, 26, 27, 0, 0)

    vs.CreateRadioButton(dlogID, 28, 'Transporter')
    vs.SetBelowItem(dlogID, 27, 28, 0, 0)

    vs.CreateRadioButton(dlogID, 29, 'Photon Torpedos')
    vs.SetBelowItem(dlogID, 28, 29, 0, 0)

    vs.CreateRadioButton(dlogID, 30, 'Phasers')
    vs.SetBelowItem(dlogID, 29, 30, 0, 0)

    # { **********  TAB CONTROL ********** }

    vs.CreateStaticText(dlogID, 35, 'Tab Control', 15)
    vs.SetBelowItem(dlogID, 15, 35, 0, 0)

    # { Tab Group 1 }
    vs.CreateGroupBox(dlogID, 50, 'Winkin', False)

    vs.CreatePushButton(dlogID, 51, 'Button 1')
    vs.SetFirstGroupItem(dlogID, 50, 51)

    vs.CreatePushButton(dlogID, 52, 'Button 2')
    vs.SetBelowItem(dlogID, 51, 52, 0, 0)

    vs.CreatePushButton(dlogID, 53, 'Button 3')
    vs.SetBelowItem(dlogID, 52, 53, 0, 0)

    # { Tab Group 2 }
    vs.CreateGroupBox(dlogID, 60, 'Blinkin', False)

    vs.CreatePushButton(dlogID, 61, 'Button 1')
    vs.SetFirstGroupItem(dlogID, 60, 61)

    vs.CreatePushButton(dlogID, 62, 'Button 2')
    vs.SetRightItem(dlogID, 61, 62, 0, 0)

    vs.CreatePushButton(dlogID, 63, 'Button 3')
    vs.SetRightItem(dlogID, 62, 63, 0, 0)

    # { Tab Group 3 }
    vs.CreateGroupBox(dlogID, 70, 'Nod', False)

    vs.CreatePushButton(dlogID, 71, 'Button 1')
    vs.SetFirstGroupItem(dlogID, 70, 71)

    vs.CreatePushButton(dlogID, 72, 'Button 2')
    vs.SetRightItem(dlogID, 71, 72, 0, 0)

    vs.CreatePushButton(dlogID, 73, 'Button 3')
    vs.SetBelowItem(dlogID, 72, 73, 0, 0)

    # { Create tab control }
    vs.CreateTabControl(dlogID, 40)
    vs.SetBelowItem(dlogID, 35, 40, 0, 0)

    # { Add the tab panes }
    vs.CreateTabPane(dlogID, 40, 50)
    vs.CreateTabPane(dlogID, 40, 60)
    vs.CreateTabPane(dlogID, 40, 70)

    return vs.RunLayoutDialog(dlogID, DialogProc)

TestNewControls()
```
