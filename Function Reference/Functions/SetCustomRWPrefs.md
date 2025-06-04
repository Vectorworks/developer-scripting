# SetCustomRWPrefs

## Description
Sets the current custom RenderWorks rendering preferences from data passed in.

```pascal
PROCEDURE SetCustomRWPrefs(
				VAR useTextures         : BOOLEAN;
				VAR useTransparency     : BOOLEAN;
				VAR useShadows          : BOOLEAN;
				VAR useRayTracing       : BOOLEAN;
				VAR useAntiAliasing     : BOOLEAN;
				VAR useDithering        : BOOLEAN;
				VAR tessellationDetail  : INTEGER;
				VAR shadowStyle         : INTEGER;
				VAR rayTracingRecursion : INTEGER);
```

```python
def vs.SetCustomRWPrefs():
    return (useTextures, useTransparency, useShadows, useRayTracing, useAntiAliasing, useDithering, tessellationDetail, shadowStyle, rayTracingRecursion)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|useTextures|BOOLEAN|   |
|useTransparency|BOOLEAN|   |
|useShadows|BOOLEAN|   |
|useRayTracing|BOOLEAN|   |
|useAntiAliasing|BOOLEAN|   |
|useDithering|BOOLEAN|   |
|tessellationDetail|INTEGER|   |
|shadowStyle|INTEGER|   |
|rayTracingRecursion|INTEGER|   |

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
