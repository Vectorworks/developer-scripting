# SetOpenGLPrefs

## Description
Sets the current OpenGL rendering preferences from data passed in.

```pascal
PROCEDURE SetOpenGLPrefs(
				VAR useTextures        : BOOLEAN;
				VAR tessellationDetail : INTEGER;
				VAR useNURBS           : BOOLEAN);
```

```python
def vs.SetOpenGLPrefs():
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
SetOpenGLPrefs(TRUE, 1, FALSE);
```
```python
import vs

# Sets the current OpenGL rendering preferences from data passed in.
useTextures, tessellationDetail, useNURBS = vs.SetOpenGLPrefs()
vs.Message('SetOpenGLPrefs returned: ' + str((useTextures, tessellationDetail, useNURBS)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
