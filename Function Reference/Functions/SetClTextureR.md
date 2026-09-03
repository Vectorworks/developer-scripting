# SetClTextureR

## Description
Procedure SetClTextureR sets the right side wall texture of the specified class.

```pascal
PROCEDURE SetClTextureR(
				className  : STRING;
				textureRef : LONGINT);
```

```python
def vs.SetClTextureR(className, textureRef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|
|textureRef|LONGINT|Texture reference index value.|

## Remarks
Sets the wall right texture of the class named className.

## Examples
```pascal
SetClTextureR('Wall', 1);
```
```python
import vs

# Procedure SetClTextureR sets the right side wall texture of the specified
# class.
className = 'None'
textureRef = 1

vs.SetClTextureR(className, textureRef)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
