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

## Examples
```pascal
BEGIN
	fieldNum := n1 + i - 1;
	IF GetDlgCtrlWidthStdCh(fieldName [fieldNum]) > labelWidth THEN labelWidth := GetDlgCtrlWidthStdCh(fieldName [fieldNum]);
END;

labelWidth := GetDlgCtrlWidthStdCh(GetPlugInString(3005));
IF labelWidth < GetDlgCtrlWidthStdCh(GetPlugInString(3006)) THEN labelWidth := GetDlgCtrlWidthStdCh(GetPlugInString(3006));
IF labelWidth < GetDlgCtrlWidthStdCh(GetPlugInString(3021)) THEN labelWidth := GetDlgCtrlWidthStdCh(GetPlugInString(3021));
IF labelWidth < GetDlgCtrlWidthStdCh(GetPlugInString(3022)) THEN labelWidth := GetDlgCtrlWidthStdCh(GetPlugInString(3022));
dialogID := CreateLayout (GetPlugInString (3003), TRUE, GetPlugInString (3001), GetPlugInString (3002));

_grpWidth_1 := GetDlgCtrlWidthStdCh( GetPluginString(3025) );{kClassLabel}
IF _grpWidth_1 < GetDlgCtrlWidthStdCh( GetPluginString(3026) ) THEN _grpWidth_1 := GetDlgCtrlWidthStdCh( GetPluginString(3026) );{kElevationLabel}
IF _grpWidth_1 < GetDlgCtrlWidthStdCh( GetPluginString(3027) ) THEN _grpWidth_1 := GetDlgCtrlWidthStdCh( GetPluginString(3027) );{kFloorHeightLabel}
IF _grpWidth_1 < GetDlgCtrlWidthStdCh( GetPluginString(3028) ) THEN _grpWidth_1 := GetDlgCtrlWidthStdCh( GetPluginString(3028) );{kUsageDataLabel}
```
```python
import vs

# Returns the width in standard characters for dialog control creation.
str = 'Example'

resultN = vs.GetDlgCtrlWidthStdCh(str)
vs.Message('GetDlgCtrlWidthStdCh returned: ' + str(resultN))
```

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
