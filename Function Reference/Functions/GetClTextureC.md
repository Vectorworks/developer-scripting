# GetClTextureC

## Description
Function GetClTextureC returns the wall center texture of the specified class.

```pascal
FUNCTION GetClTextureC(className : STRING): LONGINT;
```

```python
def vs.GetClTextureC(className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|

## Remarks
Returns the wall center textureof the class named className.

## Examples
```pascal
resultN := GetClTextureC('Wall');
```
```python
import vs

# Function GetClTextureC returns the wall center texture of the specified class.
className = 'None'

resultN = vs.GetClTextureC(className)
vs.Message('GetClTextureC returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
