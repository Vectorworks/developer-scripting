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

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
