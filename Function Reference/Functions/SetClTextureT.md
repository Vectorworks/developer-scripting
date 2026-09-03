# SetClTextureT

## Description
Procedure SetClTextureT sets the roof top texture of the specified class.

```pascal
PROCEDURE SetClTextureT(
				className  : STRING;
				textureRef : LONGINT);
```

```python
def vs.SetClTextureT(className, textureRef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|
|textureRef|LONGINT|Texture reference index value.|

## Remarks
Sets the roof top texture of the class named className.

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

# Procedure SetClTextureT sets the roof top texture of the specified class.
className = 'None'
textureRef = 1

vs.SetClTextureT(className, textureRef)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
