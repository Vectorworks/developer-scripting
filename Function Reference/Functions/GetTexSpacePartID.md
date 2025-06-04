# GetTexSpacePartID

## Description
Function GetTexSpacePartID returns the parent of the referenced texture space in an expanded object (walls or roofs).

{| class="wikitable_c"
|+ Table - Texture Space Objects
! Object !! Constant
|-
| Primary
| style="text-align:center"| 0
|-
| Secondary
| style="text-align:center"| 1
|-
| Tertiary
| style="text-align:center"| 2
|}

```pascal
FUNCTION GetTexSpacePartID(textureSpace : HANDLE): INTEGER;
```

```python
def vs.GetTexSpacePartID(textureSpace):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|

## Remarks
Returns which part (0 = Primary, 1 = Secondary, 2 = Tertiary) of the object this space belongs to (for expanded walls and roofs).

Note: GetTexMapXXX routines replace the older GetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
