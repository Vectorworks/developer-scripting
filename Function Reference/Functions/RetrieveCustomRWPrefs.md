# RetrieveCustomRWPrefs

## Description
Retrieves the current custom RenderWorks rendering preferences from data stored in the current drawing.

```pascal
PROCEDURE RetrieveCustomRWPrefs(
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
def vs.RetrieveCustomRWPrefs():
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
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
