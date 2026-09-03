# RetrieveOpenGLPrefs

## Description
Retrieves the current OpenGL rendering preferences from data stored in the current drawing.

```pascal
PROCEDURE RetrieveOpenGLPrefs(
				VAR useTextures        : BOOLEAN;
				VAR tessellationDetail : INTEGER;
				VAR useNURBS           : BOOLEAN);
```

```python
def vs.RetrieveOpenGLPrefs():
    return (useTextures, tessellationDetail, useNURBS)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|useTextures|BOOLEAN|   |
|tessellationDetail|INTEGER|   |
|useNURBS|BOOLEAN|   |

## Remarks
No longer a valid function, needs updating. (MF - Nov 11, 2015)

## Examples
```pascal
RetrieveOpenGLPrefs(TRUE, 1, FALSE);
```
```python
import vs

# Retrieves the current OpenGL rendering preferences from data stored in the
# current drawing.
useTextures, tessellationDetail, useNURBS = vs.RetrieveOpenGLPrefs()
vs.Message('RetrieveOpenGLPrefs returned: ' + str((useTextures, tessellationDetail, useNURBS)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
