# RunLayoutDialog

## Description
Displays the specified dialog and initiates the dialog event loop. The dialog event loop is specified in a procedure subroutine that is passed as a parameter to the function.

```pascal
FUNCTION RunLayoutDialog(
				dialogID : LONGINT;
				callback : PROCEDURE): LONGINT;
```

```python
def vs.RunLayoutDialog(dialogID, callback):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog to be displayed.|
|callback|PROCEDURE|The event loop subroutine for the dialog.|

## Remarks
RunLayoutDialog returns the index of the last control event (1 for OK and 2 for Cancel). The callback procedure has to be written like this:

<code lang="pas">
procedure callback(var item : longint; data :longint);
begin
message('Item: ', item, '  Data in that item: ', data);
end;
</code>

<code lang="py">
def callback(item, data):
   vs.Message('Item: ' + str(item) + '  Data in that item: '+ str(data));
	
    return item 
</code>
This function is also called before the dialog opens with a value of 2255 for item
and when the dialog closes (value 2256). 
Despite the fact that the arguments to the callback procedure are VARd (so that they should have global bindings), these variables really only have bindings within the callback procedure. Even if you declare them globally. Fact of the matter is that you cannot specify arguments when you call the callback procedure, so there's no way to establish the global bindings of the VARd arguments. Inside the callback procedure, the item argument is set to the index of the last control event. The data argument is set to values appropriate for the type of control that was activated.

Do not use the [[VS:Wait]]() function in the event handler subroutine of Layout Manager dialogs. Doing so will freeze the script, though you can force quit it with a command-period.

If you want to prevent a dialog from terminating after someone has clicked on the OK button, set item equal to -1. Note that in Python there is no output parameters. So, this value should be returned.

## Examples
ampleDialogWithTwoEdits}}

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
