# GetModifierFlags

## Description
Returns the state of option/alt, cmd/ctrl, shift keys.

```pascal
PROCEDURE GetModifierFlags(
				VAR optionFlag : BOOLEAN;
				VAR cmdFlag    : BOOLEAN;
				VAR shiftFlag  : BOOLEAN);
```

```python
def vs.GetModifierFlags():
    return (optionFlag, cmdFlag, shiftFlag)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|optionFlag|BOOLEAN|The state of the option/alt key.|
|cmdFlag|BOOLEAN|The state of the cmd/ctrl key.|
|shiftFlag|BOOLEAN|The state of the shift key.|

## Version
Availability: from Vectorworks 2025

## Category
* [Utility](../Categories/Utility.md)
