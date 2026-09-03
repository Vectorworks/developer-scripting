# OLDGetLoadDataBool

## Description
Using selector, gets load data with bool value for the parametric object
Available selectors : kDLDSelectorInclude = 1, kDLDSelHandlePosTransf = 10.

```pascal
FUNCTION OLDGetLoadDataBool(
				handle    : HANDLE;
				selector  : INTEGER;
				loadIndex : INTEGER): BOOLEAN;
```

```python
def vs.OLDGetLoadDataBool(handle, selector, loadIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|selector|INTEGER|   |
|loadIndex|INTEGER|   |

## Examples
```pascal
resultOK := OLDGetLoadDataBool(handle, 1, 2);
```
```python
import vs

# Using selector, gets load data with bool value for the parametric object
# Available selectors : kDLDSelectorInclude = 1, kDLDSelHandlePosTransf = 10.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
selector = 1
loadIndex = 1

ok = vs.OLDGetLoadDataBool(handle, selector, loadIndex)
if ok:
    vs.Message('OLDGetLoadDataBool succeeded')
else:
    vs.Message('OLDGetLoadDataBool failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
