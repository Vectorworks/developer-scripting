# Rpstr_SetValueInt

## Description
Set an integer value from the VectorScript value repository.

```pascal
PROCEDURE Rpstr_SetValueInt(
				name  : STRING;
				value : INTEGER);
```

```python
def vs.Rpstr_SetValueInt(name, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name of the value.|
|value|INTEGER|Set a value associated with the name in the VectorScript value repository.|

## Examples
```pascal
Rpstr_SetValueInt('Example', 1);
```
```python
import vs

# Set an integer value from the VectorScript value repository.
name = 'Example'
value = 1

vs.Rpstr_SetValueInt(name, value)
```

## See Also
VS Functions:
[Rpstr_RemoveValues](Rpstr_RemoveValues.md) 
| [Rpstr_RemoveValue](Rpstr_RemoveValue.md) 
| [Rpstr_GetValueBool](Rpstr_GetValueBool.md) 
| [Rpstr_SetValueBool](Rpstr_SetValueBool.md) 
| [Rpstr_GetValueInt](Rpstr_GetValueInt.md) 
| [Rpstr_SetValueInt](Rpstr_SetValueInt.md) 
| [Rpstr_GetValueReal](Rpstr_GetValueReal.md) 
| [Rpstr_SetValueReal](Rpstr_SetValueReal.md) 
| [Rpstr_GetValueStr](Rpstr_GetValueStr.md) 
| [Rpstr_SetValueStr](Rpstr_SetValueStr.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Utility](../Categories/Utility.md)
