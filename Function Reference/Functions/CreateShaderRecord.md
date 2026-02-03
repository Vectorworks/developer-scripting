# CreateShaderRecord

## Description
Creates a shader record of the desired family (1 = color, 2 = reflectivity, 3 = transparency, 4 = bump) and prototype (constants depend on family value).

Textures in Vectorworks are stored using records, called shader records.  The record values are accessed using RecordHandler routines as for other records in Vectorworks.  The first three fields of the shader record are always:

#Family
#Prototype
#Version

Family values are:

| Value | Name                  |
|-------|-----------------------|
| 1     | Color                 |
| 2     | Reflectivity          |
| 3     | Transparency          |
| 4     | Bump                  |
| 5     | Background            |
| 6     | Foreground            |
| 7     | Sketch (Artistic RW)  |

Prototype values depend on the Family value.  These are the Prototype values for each Family:

```c++
enum MaxonColorShaderPrototype {
	kMaxonColor_Plain = 40,
	kMaxonColor_Image = 41,
	kMaxonColor_Fresnel = 42,
	kMaxonColor_Noise = 43,
	kMaxonColor_Tiles = 44,
	kMaxonColor_Bricks = 45,
	kMaxonColor_Pavement = 46
};

enum MaxonReflectivityShaderPrototype {
	kMaxonReflectivity_Image = 30,
	kMaxonReflectivity_Mirror = 31,
	kMaxonReflectivity_Fresnel = 32,
	kMaxonReflectivity_Noise = 33,
	kMaxonReflectivity_Tiles = 34,
	kMaxonReflectivity_Plastic = 35,
	kMaxonReflectivity_Bricks = 36,
	kMaxonReflectivity_Pavement = 37,
	kMaxonReflectivity_Glow = 38,
	kMaxonReflectivity_Backlit = 39,
	kMaxonReflectivity_Anisotropic = 40
};

enum MaxonTransparencyShaderPrototype {
	kMaxonTransparency_Plain = 10,
	kMaxonTransparency_Color = 11,
	kMaxonTransparency_Image = 12,
	kMaxonTransparency_Glass = 13,
	kMaxonTransparency_Noise = 14,
	kMaxonTransparency_Tiles = 15,
	kMaxonTransparency_Bricks = 16,
	kMaxonTransparency_Pavement = 17,
	kMaxonTransparency_RectangularMask = 18,
	kMaxonTransparency_ImageMask = 19
};

enum MaxonBumpShaderPrototype {
	kMaxonBump_Image = 41,
	kMaxonBump_Noise = 42,
	kMaxonBump_Tiles = 43,
	kMaxonBump_Bricks = 44,
	kMaxonBump_Pavement = 45
};
```

```pascal
FUNCTION CreateShaderRecord(
				texture   : HANDLE;
				family    : LONGINT;
				prototype : LONGINT): HANDLE;
```

```python
def vs.CreateShaderRecord(texture, family, prototype):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|The shader record will be attached to this texture.|
|family|LONGINT|The kind of shader to create (1 = color, 2 = reflectivity, 3 = transparency, 4 = bump)|
|prototype|LONGINT|The specific shader within the family (constants depend on the family value).|

## Version
Availability: from VectorWorks10.1

## Category
* [Textures](../Categories/Textures.md)
