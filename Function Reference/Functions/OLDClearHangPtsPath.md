# OLDClearHangPtsPath

## Description
Clears the hang points of the specified load for the parametric object

```pascal
PROCEDURE OLDClearHangPtsPath(
				handle    : HANDLE;
				loadIndex : INTEGER);
```

```python
def vs.OLDClearHangPtsPath(handle, loadIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |

## Examples
```pascal
OLDClearHangPtsPath( ghParm, 0 );

OLDClearHangPtsPath( ghParm, kLoadScreenIndex );

OLDClearHangPtsPath( ghParm, 0 );
valid := ValidNumStr( GetRfield( ghParm, kPIOName, 'CurtHeight' ), totalHeight );
```
```python
import vs

# Clears the hang points of the specified load for the parametric object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1

vs.OLDClearHangPtsPath(handle, loadIndex)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
