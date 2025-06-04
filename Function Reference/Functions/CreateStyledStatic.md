# CreateStyledStatic

## Description
Creates a new static text field control in a dialog layout. Text will have the indicated style.<BR>
<BR>
To allow the control to size automatically to the text width, pass -1 as the width parameter of the control.<BR>
<BR>
0 = eStaticTextTypeRegular<BR>
1 = eStaticTextTypeCaption<BR>
2 = eStaticTextTypeBold,	<BR>
3 = eStaticTextTypeReduced<BR>
<BR>

```pascal
PROCEDURE CreateStyledStatic(
				dialogID          : LONGINT;
				componentID       : LONGINT;
				text              : STRING;
				widthInCharacters : INTEGER;
				style             : INTEGER);
```

```python
def vs.CreateStyledStatic(dialogID, componentID, text, widthInCharacters, style):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|text|STRING|   |
|widthInCharacters|INTEGER|   |
|style|INTEGER|Type of this static text control. One of:||0 = eStaticTextTypeRegular|1 = eStaticTextTypeCaption|2 = eStaticTextTypeBold,|3 = eStaticTextTypeReduced,|101-116 = Custom size, normal|201-216 = Custom size, bold|

## Examples
```pascal
PROCEDURE Example;
VAR
   dialog1 :INTEGER;
   result  :INTEGER;
PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
END;
BEGIN
   dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
   CreateEditText(dialog1, 4, 'default text', 16);
   CreateStyledStatic(dialog1, 5, 'default text', 16, 2);
   SetFirstLayoutItem(dialog1, 4);
   SetBelowItem(dialog1, 4, 5, 0, 0);
   result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```

## See Also
VS Functions:
[CreateStaticText](CreateStaticText.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
