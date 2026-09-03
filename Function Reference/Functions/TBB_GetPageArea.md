# TBB_GetPageArea

## Description
Gets the page area of the selected layer in inches

```pascal
PROCEDURE TBB_GetPageArea(
				LayerHand      : HANDLE;
				VAR PageWidth  : REAL;
				VAR PageHeight : REAL);
```

```python
def vs.TBB_GetPageArea(LayerHand):
    return (PageWidth, PageHeight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|LayerHand|HANDLE|   |
|PageWidth|REAL|   |
|PageHeight|REAL|   |

## Examples
```pascal
TBB_GetPageArea(ActLayer, paperHorizDim, paperVertDim);
```
```python
import vs

# Gets the page area of the selected layer in inches.
LayerHand = vs.ActLayer()  # handle to the active design layer

PageWidth, PageHeight = vs.TBB_GetPageArea(LayerHand)
vs.Message('TBB_GetPageArea returned: ' + str((PageWidth, PageHeight)))
```

## Version
Availability: from Vectorworks 2019.1

## Category
* [Utility](../Categories/Utility.md)
