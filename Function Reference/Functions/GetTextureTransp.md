# GetTextureTransp

## Description
Function GetTextureTransp returns the degree of transparency applied to the referenced texture. It is expressed as a percentage with 0 creating an opaque texture.

```pascal
FUNCTION GetTextureTransp(texture : HANDLE): INTEGER;
```

```python
def vs.GetTextureTransp(texture):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|Handle to texture.|

## Remarks
Percentage value - 0 equals opaque

## Version
GetTextureTransp is obsolete as of VectorWorks9.0<P>


Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
