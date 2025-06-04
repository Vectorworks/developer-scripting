# OLDGetConstructMat

## Description
Returns the universal and the localized names of the construction material at the given index.

```pascal
PROCEDURE OLDGetConstructMat(
				materialIndex     : LONGINT;
				VAR UniversalName : STRING;
				VAR LocalizedName : STRING);
```

```python
def vs.OLDGetConstructMat(materialIndex):
    return (UniversalName, LocalizedName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialIndex|LONGINT|   |
|UniversalName|STRING|   |
|LocalizedName|STRING|   |

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
