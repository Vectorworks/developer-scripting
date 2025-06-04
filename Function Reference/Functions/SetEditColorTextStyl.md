# SetEditColorTextStyl

## Description
Set styles for the control, providing or requesting data. More info of the choices can be found in the developer.vectorworks.net

```pascal
FUNCTION SetEditColorTextStyl(
				dialogID      : LONGINT;
				itemID        : LONGINT;
				strStyle      : DYNARRAY[] of CHAR;
				VAR outValue  : DYNARRAY[] of CHAR;
				VAR outParam2 : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.SetEditColorTextStyl(dialogID, itemID, strStyle):
    return (BOOLEAN, outValue, outParam2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|strStyle|DYNARRAY[] of CHAR|The parameter configures the control by key-value pairs configuring the control. It can point to a file full path containing configuration for reusability|
|outValue|DYNARRAY[] of CHAR|Some set style commands produce value. The value will be packed up in a string which the user must take care as needed.|
|outParam2|DYNARRAY[] of CHAR|Some style commands return parameter, The value will be packed up in a string which the user must take care as needed.|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
