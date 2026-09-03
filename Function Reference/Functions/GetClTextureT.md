# GetClTextureT

## Description
Function GetClTextureT returns the roof top texture of the specified class.

```pascal
FUNCTION GetClTextureT(className : STRING): LONGINT;
```

```python
def vs.GetClTextureT(className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|

## Remarks
Returns the roof top texture of the class named className.

## Examples
```pascal
BEGIN
regtex := GetClTextureG(roof_class);
rooftex := GetClTextureT(roof_class);
IF ((rooftex = 0) & (regtex <> 0)) THEN SetClTextureT(roof_class,regtex);
END;
```
```python
import vs

# Function GetClTextureT returns the roof top texture of the specified class.
className = 'None'

resultN = vs.GetClTextureT(className)
vs.Message('GetClTextureT returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
