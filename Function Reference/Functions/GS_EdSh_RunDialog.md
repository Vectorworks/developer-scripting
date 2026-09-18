# GS_EdSh_RunDialog

## Description
Runs an edit shader dialog layout.

```pascal
PROCEDURE GS_EdSh_RunDialog(
				VAR userHitOK  : BOOLEAN;
				libraryDataPtr : LONGINT);
```

```python
def vs.GS_EdSh_RunDialog(libraryDataPtr):
    return userHitOK
```

## Parameters
|Name|Type|Description|
|---|---|---|
|userHitOK|BOOLEAN|   |
|libraryDataPtr|LONGINT|   |

## Examples
```pascal
GS_EdSh_RunDialog(TRUE, 1);
```
```python
import vs

# Runs an edit shader dialog layout.
libraryDataPtr = 1

result = vs.GS_EdSh_RunDialog(libraryDataPtr)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
