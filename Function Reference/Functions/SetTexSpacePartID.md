# SetTexSpacePartID

## Description
Procedure SetTexSpacePartID sets the parent of the referenced texture space in an expanded object (walls or roofs).

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
PROCEDURE SetTexSpacePartID(
				textureSpace : HANDLE;
				partID       : INTEGER);
```

```python
def vs.SetTexSpacePartID(textureSpace, partID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|partID|INTEGER|Part ID of texture space parent.|

## Remarks
Sets which part (0 = Primary, 1 = Secondary, 2 = Tertiary) of the object this space belongs to (for expanded walls and roofs).

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
