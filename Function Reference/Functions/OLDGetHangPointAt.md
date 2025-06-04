# OLDGetHangPointAt

## Description
Get hang point for given index of the specified load for the parametric object

```pascal
PROCEDURE OLDGetHangPointAt(
				handle      : HANDLE;
				loadIndex   : INTEGER;
				pointIndex  : LONGINT;
				VAR point   : VECTOR;
				VAR hasLoad : BOOLEAN);
```

```python
def vs.OLDGetHangPointAt(handle, loadIndex, pointIndex):
    return (point, hasLoad)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |
|pointIndex|LONGINT|   |
|point|VECTOR|   |
|hasLoad|BOOLEAN|   |

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
