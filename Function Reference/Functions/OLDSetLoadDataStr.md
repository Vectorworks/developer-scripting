# OLDSetLoadDataStr

## Description
Using selector, sets load data with string value for the parametric object
Available selectors : kDLDSelectorGroupName = 2, kDLDSelectorLoadID = 3, kDLDSelectorLoadName = 4, kDLDSelectorPrmLoadID = 6, kDLDSelectorPrmName = 7, kDLDSelectorPrmWeight = 8, kDLDSelPrmTotalDistWght = 9.
<br />
Selector kDLDSelectorGroupName determinate the category, where the load will be displayed in the overview. This selector can be used with one of the following values: 'Audio', 'Video', 'Light', 'Decoration' (displayed as Scenery), 'Cable', 'Truss' and 'LoadingPoint'.

```pascal
PROCEDURE OLDSetLoadDataStr(
				handle    : HANDLE;
				selector  : INTEGER;
				value     : STRING;
				loadIndex : INTEGER);
```

```python
def vs.OLDSetLoadDataStr(handle, selector, value, loadIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|selector|INTEGER|   |
|value|STRING|   |
|loadIndex|INTEGER|   |

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
