# SetClTextureC

## Description
Procedure SetClTextureC sets the wall center texture of the specified class.

```pascal
PROCEDURE SetClTextureC(
				className  : STRING;
				textureRef : LONGINT);
```

```python
def vs.SetClTextureC(className, textureRef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|
|textureRef|LONGINT|Texture reference index value.|

## Remarks
Sets the wall center texture of the class named className.

## Examples
```pascal
SetClTextureC('Wall', 1);
```
```python
import vs

# Procedure SetClTextureC sets the wall center texture of the specified class.
className = 'None'
textureRef = 1

vs.SetClTextureC(className, textureRef)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
