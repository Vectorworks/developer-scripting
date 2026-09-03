# GS_EdSh_ConstructLayout

## Description
Creates a dialog layout for editing a shader's parameter values.

```pascal
PROCEDURE GS_EdSh_ConstructLayout(
				shaderNameCStr     : LONGINT;
				paramsPtr          : LONGINT;
				VAR libraryDataPtr : LONGINT);
```

```python
def vs.GS_EdSh_ConstructLayout(shaderNameCStr, paramsPtr):
    return libraryDataPtr
```

## Parameters
|Name|Type|Description|
|---|---|---|
|shaderNameCStr|LONGINT|   |
|paramsPtr|LONGINT|   |
|libraryDataPtr|LONGINT|   |

## Examples
```pascal
GS_EdSh_ConstructLayout(1, 2, 3);
```
```python
import vs

# Creates a dialog layout for editing a shader's parameter values.
shaderNameCStr = 'Example'
paramsPtr = 1

result = vs.GS_EdSh_ConstructLayout(shaderNameCStr, paramsPtr)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
