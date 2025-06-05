==== VectorScript ====
```pascal
PROCEDURE dialog1_Main;
	VAR
	dialog1 :INTEGER;
	result : INTEGER;
	PROCEDURE dialog1_Setup;
	BEGIN
	dialog1 := CreateLayout('Swap Pane Test', FALSE, 'OK', 'Cancel');
	CreatePulldownMenu(dialog1,  4, 15);
	CreateGroupBox    (dialog1,  5, 'Control', TRUE);

	CreateSwapControl (dialog1,  6);

	CreateGroupBox    (dialog1,  7, '', TRUE);
	CreatePushButton  (dialog1,  8, 'Button 1.0');

	CreateGroupBox    (dialog1,  9, '', TRUE);
	CreatePushButton  (dialog1, 10, 'Button 2.0');
	CreatePushButton  (dialog1, 11, 'Button 2.1');

	CreateGroupBox    (dialog1, 12, '', TRUE);
	CreatePushButton  (dialog1, 13, 'Button 3.0');
	CreatePushButton  (dialog1, 14, 'Button 3.1');
	CreatePushButton  (dialog1, 15, 'Button 3.2');

	CreateGroupBox    (dialog1, 16, '', TRUE);
	CreatePushButton  (dialog1, 17, 'Button 4.0');
	CreatePushButton  (dialog1, 18, 'Button 4.1');
	CreatePushButton  (dialog1, 19, 'Button 4.2');
	CreatePushButton  (dialog1, 20, 'Button 4.3');

	SetFirstLayoutItem(dialog1,  4);
	SetBelowItem      (dialog1,  4,  5,  0, 0);
	SetFirstGroupItem (dialog1,  5,  6);

	CreateSwapPane    (dialog1,  6,  7);
	SetFirstGroupItem (dialog1,  7,  8);

	CreateSwapPane    (dialog1,  6,  9);
	SetFirstGroupItem (dialog1,  9, 10);
	SetBelowItem      (dialog1, 10, 11,  0, 0);

	CreateSwapPane    (dialog1,  6, 12);
	SetFirstGroupItem (dialog1, 12, 13);
	SetBelowItem      (dialog1, 13, 14,  0, 0);
	SetBelowItem      (dialog1, 14, 15,  0, 0);

	CreateSwapPane    (dialog1,  6, 16);
	SetFirstGroupItem (dialog1, 16, 17);
	SetBelowItem      (dialog1, 17, 18,  0, 0);
	SetBelowItem      (dialog1, 18, 19,  0, 0);
	SetBelowItem      (dialog1, 19, 20,  0, 0);
	END;

	PROCEDURE dialog1_Handler(VAR item: LONGINT; data: LONGINT);
	BEGIN
		CASE item OF
		SetupDialogC:
		BEGIN
		result := 0;
		END;

		100:	DisplayTabPane(dialog1, 10, 1);  { Display pane 1 }
		101:	DisplayTabPane(dialog1, 10, 2);  { Display pane 2 }
		102:	DisplayTabPane(dialog1, 10, 3);  { Display pane 3 }

		END;
	END;
	
BEGIN
dialog1_Setup;
IF RunLayoutDialog(dialog1, dialog1_Handler) = 1 THEN 
	BEGIN
	END;

END;

RUN(dialog1_Main);
```

==== Python ====
```python
def dialog1_Setup():
	global dialog1
	dialog1 = vs.CreateLayout('Swap Pane Test', False, 'OK', 'Cancel')
	vs.CreatePullDownMenu(dialog1,  4, 15)
	vs.CreateGroupBox    (dialog1,  5, 'Control', True)

	vs.CreateSwapControl (dialog1,  6)

	vs.CreateGroupBox    (dialog1,  7, '', True)
	vs.CreatePushButton  (dialog1,  8, 'Button 1.0')

	vs.CreateGroupBox    (dialog1,  9, '', True)
	vs.CreatePushButton  (dialog1, 10, 'Button 2.0')
	vs.CreatePushButton  (dialog1, 11, 'Button 2.1')

	vs.CreateGroupBox    (dialog1, 12, '', True)
	vs.CreatePushButton  (dialog1, 13, 'Button 3.0')
	vs.CreatePushButton  (dialog1, 14, 'Button 3.1')
	vs.CreatePushButton  (dialog1, 15, 'Button 3.2')

	vs.CreateGroupBox    (dialog1, 16, '', True)
	vs.CreatePushButton  (dialog1, 17, 'Button 4.0')
	vs.CreatePushButton  (dialog1, 18, 'Button 4.1')
	vs.CreatePushButton  (dialog1, 19, 'Button 4.2')
	vs.CreatePushButton  (dialog1, 20, 'Button 4.3')

	vs.SetFirstLayoutItem(dialog1,  4)
	vs.SetBelowItem      (dialog1,  4,  5,  0, 0)
	vs.SetFirstGroupItem (dialog1,  5,  6)

	vs.CreateSwapPane    (dialog1,  6,  7)
	vs.SetFirstGroupItem (dialog1,  7,  8)

	vs.CreateSwapPane    (dialog1,  6,  9)
	vs.SetFirstGroupItem (dialog1,  9, 10)
	vs.SetBelowItem      (dialog1, 10, 11,  0, 0)

	vs.CreateSwapPane    (dialog1,  6, 12)
	vs.SetFirstGroupItem (dialog1, 12, 13)
	vs.SetBelowItem      (dialog1, 13, 14,  0, 0)
	vs.SetBelowItem      (dialog1, 14, 15,  0, 0)

	vs.CreateSwapPane    (dialog1,  6, 16)
	vs.SetFirstGroupItem (dialog1, 16, 17)
	vs.SetBelowItem      (dialog1, 17, 18,  0, 0)
	vs.SetBelowItem      (dialog1, 18, 19,  0, 0)
	vs.SetBelowItem      (dialog1, 19, 20,  0, 0)


def dialog1_Handler( item , data):
	if item == SetupDialogC:
		result = 0
	elif item == 100:	
		vs.DisplayTabPane(dialog1, 10, 1)
	elif item == 101:	
		vs.DisplayTabPane(dialog1, 10, 2)
	elif item == 102:
		vs.DisplayTabPane(dialog1, 10, 3) 




def dialog1_Main():	
	if vs.RunLayoutDialog(dialog1, dialog1_Handler) == 1:
		pass

global	SetupDialogC	
SetupDialogC = 12255
dialog1 = 0
dialog1_Setup()
dialog1_Main()
```
