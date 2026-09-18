# GetClTextureR

## Description
Function GetClTextureR returns the right side wall texture of the specified class.

```pascal
FUNCTION GetClTextureR(className : STRING): LONGINT;
```

```python
def vs.GetClTextureR(className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|

## Remarks
Returns the wall right texture of the class named className.

## Examples
```pascal
resultN := GetClTextureR('Wall');
```
```python
import vs

# Function GetClTextureR returns the right side wall texture of the specified
# class.
className = 'None'

resultN = vs.GetClTextureR(className)
vs.Message('GetClTextureR returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
