# SetTextureTransp

## Description
Procedure SetTextureTransp sets the degree of transparency applied to the referenced texture.  The transparency value is expressed in the range of 0-100, with 0 equaling opaque and 100 equaling transparent.

```pascal
PROCEDURE SetTextureTransp(
				texture      : HANDLE;
				transparency : INTEGER);
```

```python
def vs.SetTextureTransp(texture, transparency):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|Handle to texture.|
|transparency|INTEGER|Transparency setting for texture.|

## Remarks
Percentage value - 0 equals opaque

## Version
SetTextureTransp is obsolete as of VectorWorks9.0<P>


Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
