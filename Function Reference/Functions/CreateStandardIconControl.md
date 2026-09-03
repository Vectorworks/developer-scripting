# CreateStandardIconControl

## Description
Creates a standard icon control, which is used to display the application icon or an alert icon. Valid values for iconNumber are:
0 - VectorWorks application icon
1 - Informational icon
2 - Stop icon
3 - Exclamation mark (warning) icon
4 - Question icon

```pascal
PROCEDURE CreateStandardIconControl(
				dialogID      : LONGINT;
				iconControlID : LONGINT;
				iconNumber    : INTEGER);
```

```python
def vs.CreateStandardIconControl(dialogID, iconControlID, iconNumber):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|iconControlID|LONGINT|ID of the control within the dialog|
|iconNumber|INTEGER|Constant, listed above, indicating which icon to display.|

## Remarks
Should show image of each icon.

## Examples
[ComplexDialogLayout2](examples/ComplexDialogLayout2.md)

```pascal
{create controls}
CreateStandardIconControl( dialog, kUnnamed, 1 );
CreateStaticText( dialog, klPrompt, GetStr(klPrompt), 60 );
CreateCheckBox( dialog, kbDoNotShow, GetStr(kbDoNotShow) );
```
```python
import vs

# Creates a standard icon control, which is used to display the application
# icon or an alert icon.
dialogID = 1
iconControlID = 2
iconNumber = 3

vs.CreateStandardIconControl(dialogID, iconControlID, iconNumber)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks11.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
