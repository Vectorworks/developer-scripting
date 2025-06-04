# AddChoice

## Description
Adds an item to the component's choices.

The valid components are created by [[VS:CreatePullDownMenu| CreatePullDownMenu]], [[VS:CreatePullDownMenuGroupBox| CreatePullDownMenuGroupBox]], [[VS:CreateListBox| CreateListBox]], [[VS:CreateListBoxN| CreateListBoxN]].

```pascal
PROCEDURE AddChoice(
				dialogID    : LONGINT;
				componentID : LONGINT;
				choiceText  : STRING;
				itemIndex   : INTEGER);
```

```python
def vs.AddChoice(dialogID, componentID, choiceText, itemIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the component that contains the choices.|
|choiceText|STRING|The text for the item that is about to be added.|
|itemIndex|INTEGER|The index after which the new item is to be added.|

## Remarks
For components created by [[VS:CreateEnhancedPullDownMenu| CreateEnhancedPullDownMenu]], [[VS:InsertEnhancedPullDownMenuItem| InsertEnhancedPullDownMenuItem]] should be used.

## Examples
alogLayoutPulldownMenu}}

## See Also
For further information, please check out:
[CreatePullDownMenu| CreatePullDownMenu](CreatePullDownMenu|%20CreatePullDownMenu.md)

[CreatePullDownMenuGroupBox| CreatePullDownMenuGroupBox](CreatePullDownMenuGroupBox|%20CreatePullDownMenuGroupBox.md)

[CreateListBox| CreateListBox](CreateListBox|%20CreateListBox.md)

[CreateListBoxN| CreateListBoxN](CreateListBoxN|%20CreateListBoxN.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
