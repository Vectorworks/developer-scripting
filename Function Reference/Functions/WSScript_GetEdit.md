# WSScript_GetEdit

## Description
This function must be used inside a worksheet script called by 'RunScriptEdit' worksheet formula. It will tell the script when a value has been change and what's the value. Use 'WSScript_GetEditObj' to get the value.

```pascal
FUNCTION WSScript_GetEdit(VAR outNewValue : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.WSScript_GetEdit():
    return (BOOLEAN, outNewValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outNewValue|DYNARRAY[] of CHAR|The new value for the cell as inputted by the user.|

## See Also
VS Functions:
[WSScript_GetEditObj](WSScript_GetEditObj.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Worksheets](../Categories/Worksheets.md)
