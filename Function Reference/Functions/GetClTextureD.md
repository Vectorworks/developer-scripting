# GetClTextureD

## Description
Function GetClTextureD returns the roof dormer texture of the specified class.

```pascal
FUNCTION GetClTextureD(className : STRING): LONGINT;
```

```python
def vs.GetClTextureD(className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|

## Remarks
Returns the roof dormer texture of the class named className.

## Examples
```pascal
resultN := GetClTextureD('Wall');
```
```python
import vs

# Function GetClTextureD returns the roof dormer texture of the specified class.
className = 'None'

resultN = vs.GetClTextureD(className)
vs.Message('GetClTextureD returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
