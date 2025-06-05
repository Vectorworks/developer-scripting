# New Functions 

[Vectorworks 2010 New Functions](../VS/Vectorworks%202010%20New%20Functions.md)

# List of deprecated functions

## Dialogs - Classic

* __AddButton__
* __AddChoiceItem__
* __AddField__
* __AddGroupBox__
* __AddHelpItem__
* __BeginDialog__
* __ClrDialog__
* __DialogEvent__
* __DrawDialog__
* __EndDialog__
* __GetDialog__
* __SetTitle__

## Dialogs - Handler

* __DelChoice__
* __GetChoiceStr__
* __GetField__
* __GetSelChoice__
* __InsertChoice__
* __ItemSel__
* __NumChoices__
* __SelChoice__
* __SelField__
* __SetField__
* __SetHelpString__
* __SetItem__
* __SetItemEnable__
* __SetTextEditable__

## Textures

* __GetTexMapBool__
* __GetTexMapInt__
* __GetTexMapReal__
* __GetTextureRef__
* __SetDefaultTexMap__
* __SetTexMapBool__
* __SetTexMapInt__
* __SetTexMapReal__
* __SetTextureRef__

# Layout Manager API Match Table

## Dialogs - Classic

| Legacy APIs | Layout Manager APIs |
|-------------|---------------------|
| __AddButton__ | [CreatePushButton](../../Function%20Reference/Functions/CreatePushButton.md)<br>[CreateCheckBox](../../Function%20Reference/Functions/CreateCheckBox.md)<br>[CreateRadioButton](../../Function%20Reference/Functions/CreateRadioButton.md) |
| __AddChoiceItem__ | [CreatePullDownMenu](../../Function%20Reference/Functions/CreatePullDownMenu.md) |
| __AddField__ | [CreateStaticText](../../Function%20Reference/Functions/CreateStaticText.md)<br>[CreateEditText](../../Function%20Reference/Functions/CreateEditText.md)<br>[CreateEditTextBox](../../Function%20Reference/Functions/CreateEditTextBox.md)<br>[CreateEditInteger](../../Function%20Reference/Functions/CreateEditInteger.md)<br>[CreateEditReal](../../Function%20Reference/Functions/CreateEditReal.md) |
| __AddGroupBox__ | [CreateGroupBox](../../Function%20Reference/Functions/CreateGroupBox.md)<br>[CreateCheckBoxGroupBox](../../Function%20Reference/Functions/CreateCheckBoxGroupBox.md)<br>[CreateRadioButtonGroupBox](../../Function%20Reference/Functions/CreateRadioButtonGroupBox.md) |
| __AddHelpItem__ | [SetHelpText](../../Function%20Reference/Functions/SetHelpText.md) |
| __BeginDialog__ | - |
| __ClrDialog__ | - |
| __DialogEvent__ | - |
| __DrawDialog__ | - |
| __EndDialog__ | - |
| __GetDialog__ | - |
| __SetTitle__ | - |

## Dialogs - Handler

| Legacy APIs | Layout Manager APIs |
|-------------|---------------------|
| __DelChoice__ | [RemoveChoice](../../Function%20Reference/Functions/RemoveChoice.md) |
| __GetChoiceStr__ | [GetChoiceText](../../Function%20Reference/Functions/GetChoiceText.md) |
| __GetField__ | [GetItemText](../../Function%20Reference/Functions/GetItemText.md)<br>[GetMultilineText](../../Function%20Reference/Functions/GetMultilineText.md) |
| __GetSelChoice__ | [GetSelectedChoiceInfo](../../Function%20Reference/Functions/GetSelectedChoiceInfo.md) |
| __InsertChoice__ | [AddChoice](../../Function%20Reference/Functions/AddChoice.md) |
| __ItemSel__ | [GetBooleanItem](../../Function%20Reference/Functions/GetBooleanItem.md) |
| __NumChoices__ | [GetChoiceCount](../../Function%20Reference/Functions/GetChoiceCount.md) |
| __SelChoice__ | [SelectChoice](../../Function%20Reference/Functions/SelectChoice.md) |
| __SelField__ | [SelectEditText](../../Function%20Reference/Functions/SelectEditText.md) |
| __SetField__ | [SetItemText](../../Function%20Reference/Functions/SetItemText.md) |
| __SetItem__ | [SetBooleanItem](../../Function%20Reference/Functions/SetBooleanItem.md) |
| __SetHelpString__ | [SetHelpText](../../Function%20Reference/Functions/SetHelpText.md) |
| __SetItemEnable__ | [EnableItem](../../Function%20Reference/Functions/EnableItem.md) |
| __SetTextEditable__ | [EnableTextEdit](../../Function%20Reference/Functions/EnableTextEdit.md) |

## Textures

| Legacy APIs | Layout Manager APIs |
|-------------|---------------------|
| __GetTexMapBool__ | [GetTexMapBoolN](../../Function%20Reference/Functions/GetTexMapBoolN.md) |
| __GetTexMapInt__ | [GetTexMapIntN](../../Function%20Reference/Functions/GetTexMapIntN.md) |
| __GetTexMapReal__ | [GetTexMapRealN](../../Function%20Reference/Functions/GetTexMapRealN.md) |
| __GetTextureRef__ | [GetTextureRefN](../../Function%20Reference/Functions/GetTextureRefN.md) |
| __SetDefaultTexMap__ | [SetDefaultTexMapN](../../Function%20Reference/Functions/SetDefaultTexMapN.md) |
| __SetTexMapBool__ | [SetTexMapBoolN](../../Function%20Reference/Functions/SetTexMapBoolN.md) |
| __SetTexMapInt__ | [SetTexMapIntN](../../Function%20Reference/Functions/SetTexMapIntN.md) |
| __SetTexMapReal__ | [SetTexMapRealN](../../Function%20Reference/Functions/SetTexMapRealN.md) |
| __SetTextureRef__ | [SetTextureRefN](../../Function%20Reference/Functions/SetTextureRefN.md) |

