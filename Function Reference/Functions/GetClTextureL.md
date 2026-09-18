# GetClTextureL

## Description
Function GetClTextureL returns the left side wall texture of the specified class.

```pascal
FUNCTION GetClTextureL(className : STRING): LONGINT;
```

```python
def vs.GetClTextureL(className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|

## Remarks
Returns the wall left texture of the class named className.

## Examples
```pascal
resultN := GetClTextureL('Wall');
```
```python
import vs

# Function GetClTextureL returns the left side wall texture of the specified
# class.
className = 'None'

resultN = vs.GetClTextureL(className)
vs.Message('GetClTextureL returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
