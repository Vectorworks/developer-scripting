# SetClTextureG

## Description
Procedure SetClTextureG sets the generic texture of the specified class.

```pascal
PROCEDURE SetClTextureG(
				className  : STRING;
				textureRef : LONGINT);
```

```python
def vs.SetClTextureG(className, textureRef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|
|textureRef|LONGINT|Texture reference index value.|

## Remarks
Sets the generic texture of the class named className.

## Examples
```pascal
SetClTextureG('Wall', 1);
```
```python
import vs

# Procedure SetClTextureG sets the generic texture of the specified class.
className = 'None'
textureRef = 1

vs.SetClTextureG(className, textureRef)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
