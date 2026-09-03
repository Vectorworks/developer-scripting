# GS_EdSh_PopulateMenu

## Description
Adds menu items to a popup in an edit shader dialog.

```pascal
PROCEDURE GS_EdSh_PopulateMenu(
				itemID         : LONGINT;
				numStrings     : LONGINT;
				cStringsArray  : LONGINT;
				libraryDataPtr : LONGINT);
```

```python
def vs.GS_EdSh_PopulateMenu(itemID, numStrings, cStringsArray, libraryDataPtr):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|itemID|LONGINT|   |
|numStrings|LONGINT|   |
|cStringsArray|LONGINT|   |
|libraryDataPtr|LONGINT|   |

## Examples
```pascal
GS_EdSh_PopulateMenu(1, 2, 3, 10);
```
```python
import vs

# Adds menu items to a popup in an edit shader dialog.
itemID = 1
numStrings = 5
cStringsArray = 2
libraryDataPtr = 3

vs.GS_EdSh_PopulateMenu(itemID, numStrings, cStringsArray, libraryDataPtr)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Textures](../Categories/Textures.md)
