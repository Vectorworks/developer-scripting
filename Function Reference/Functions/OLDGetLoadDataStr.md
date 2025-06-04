# OLDGetLoadDataStr

## Description
Using selector, gets load data with string value for the parametric object.
Available selectors : kDLDSelectorInclude = 1, kDLDSelectorGroupName = 2, kDLDSelectorLoadID = 3, kDLDSelectorLoadName = 4, kDLDSelectorPrmLoadID = 6, kDLDSelectorPrmName = 7, kDLDSelectorPrmWeight = 8, kDLDSelPrmTotalDistWght = 9.

```pascal
FUNCTION OLDGetLoadDataStr(
				handle    : HANDLE;
				selector  : INTEGER;
				loadIndex : INTEGER): STRING;
```

```python
def vs.OLDGetLoadDataStr(handle, selector, loadIndex):
    return STRING
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
