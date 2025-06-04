# GetDlgCtrlWidthStdCh

## Description
Returns the width in standard characters for dialog control creation. <BR>
<BR>
The width is different than the number of symbols (Len) as in some languages (Japanese for example) the symbols are very different in size on the dialog.<BR>
<BR>
E.g. CreateStaticText

```pascal
FUNCTION GetDlgCtrlWidthStdCh(str : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.GetDlgCtrlWidthStdCh(str):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|DYNARRAY[] of CHAR|The string used to calculate the std character count.|

## See Also
VS Functions:
[CreateStaticText](CreateStaticText.md) 
| [CreateCenteredStaticText](CreateCenteredStaticText.md) 
| [CreateStyledStatic](CreateStyledStatic.md) 
| [CreateEditInteger](CreateEditInteger.md) 
| [CreateEditReal](CreateEditReal.md) 
| [CreateEditText](CreateEditText.md) 
| [CreateEditTextBox](CreateEditTextBox.md) 
| [CreateListBox](CreateListBox.md) 
| [CreateListBoxN](CreateListBoxN.md) 
| [CreateLB](CreateLB.md) 
| [CreatePullDownMenu](CreatePullDownMenu.md) 
| [CreateEnhancedPullDownMenu](CreateEnhancedPullDownMenu.md) 
| [CreateColorPopup](CreateColorPopup.md) 
| [CreatePullDownMenuGroupBox](CreatePullDownMenuGroupBox.md) 
| [CreateTreeControl](CreateTreeControl.md) 
| [CreateClassPullDownMenu](CreateClassPullDownMenu.md) 
| [CreateDesignLayerPullDownMenu](CreateDesignLayerPullDownMenu.md) 
| [CreateSheetLayerPullDownMenu](CreateSheetLayerPullDownMenu.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
