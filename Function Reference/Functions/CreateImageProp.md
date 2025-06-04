# CreateImageProp

## Description
Create an image prop from the options specified.  

The texture resource and optional symbol created will use names derived from the propName parameter.  If those names are being used then unique names will be assigned.  If enforceImageAspectRatio is true, depending on deriveWidthFromHeight the prop width/height will be derived from the prop height/width and the texture?s image aspect ratio. Otherwise the height and width can be set independently of the texture?s image aspect ratio.

```pascal
FUNCTION CreateImageProp(
				propName                : STRING;
				textureRef              : LONGINT;
				height                  : REAL;
				width                   : REAL;
				enforceImageAspectRatio : BOOLEAN;
				crossedPlanes           : BOOLEAN;
				createPlugin            : BOOLEAN;
				autoRotate              : BOOLEAN;
				createSymbol            : BOOLEAN): HANDLE;
```

```python
def vs.CreateImageProp(propName, textureRef, height, width, enforceImageAspectRatio, crossedPlanes, createPlugin, autoRotate, createSymbol):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|propName|STRING|   |
|textureRef|LONGINT|   |
|height|REAL|   |
|width|REAL|   |
|enforceImageAspectRatio|BOOLEAN|   |
|crossedPlanes|BOOLEAN|   |
|createPlugin|BOOLEAN|   |
|autoRotate|BOOLEAN|   |
|createSymbol|BOOLEAN|   |

## Version
Availability: from VectorWorks11.5

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
