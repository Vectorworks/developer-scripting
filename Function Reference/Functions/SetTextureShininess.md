# SetTextureShininess

## Description
Procedure SetTextureShininess sets the shininess value of the referenced texture. The value is expressed as a percentage value in a range of 0-100 with 0 equaling &quot;Dull&quot;.

```pascal
PROCEDURE SetTextureShininess(
				texture   : HANDLE;
				shininess : INTEGER);
```

```python
def vs.SetTextureShininess(texture, shininess):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|Handle to texture.|
|shininess|INTEGER|Shininess setting for texture.|

## Remarks
Percentage value - 0 equals dull

## Examples
```pascal
SetTextureShininess(texture, 1);
```
```python
import vs

# Procedure SetTextureShininess sets the shininess value of the referenced
# texture.
texture = vs.FSActLayer()  # handle to the first selected object on the active layer
shininess = 1

vs.SetTextureShininess(texture, shininess)
```

## Version
SetTextureShininess is obsolete as of VectorWorks9.0<P>

Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
