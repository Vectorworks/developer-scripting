# GetLevelTypeName

## Description
Returns the name of the nth Level Type in the file. For example, if 3 is passed in, it will return the name of the 3rd Level Type in the file.

```pascal
FUNCTION GetLevelTypeName(index : INTEGER): STRING;
```

```python
def vs.GetLevelTypeName(index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the level type whose name is desired.|

## Examples
```pascal
VAR

levelTypeName:STRING;

BEGIN

levelTypeName:=GetLayerLevelTypeName(2);
```

## See Also
VS Functions:
[GetNumLayerLevelTypes](GetNumLayerLevelTypes.md) 
| [SetLevelTypeName](SetLevelTypeName.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Layers](../Categories/Layers.md)
