==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
dialog1 :INTEGER;
result  :INTEGER;
PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
SetColorChoice(dialog1, 4, 1242);
END;
1:
BEGIN
GetColorChoice(dialog1, 4, result);
AlrtDialog(Concat('color index: ', result));
END;
END;
END;
BEGIN
dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
CreateColorPopup(dialog1, 4, 24);
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```

==== Python ====
```python
def Dialog_Handler(item , data ):
	if item == SetupDialogC:
		vs.SetColorChoice(dialog1, 4, 1242)
	elif item == 1:
		result = vs.GetColorChoice(dialog1, 4)
		vs.AlrtDialog(vs.Concat('color index: ', result));

def Example():
	global dialog1
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateColorPopup(dialog1, 4, 24)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)

global SetupDialogC
SetupDialogC = 12255
dialog1 = 0
Example()
```
