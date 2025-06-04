# SetClTextStyleRef

## Description
Function SetClTextStyleRef sets the text style of the specified class.  The integer style is the internal index of the text style.

```pascal
PROCEDURE SetClTextStyleRef(
				className    : STRING;
				textStyleRef : LONGINT);
```

```python
def vs.SetClTextStyleRef(className, textStyleRef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class|
|textStyleRef|LONGINT|text style reference id|

## See Also
VS Functions:
[SetClUseTextStyle](SetClUseTextStyle.md) 
| [GetClUseTextStyle](GetClUseTextStyle.md) 
| [GetClTextStyleRef](GetClTextStyleRef.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Classes](../Categories/Classes.md)
