# DLDSetLoadDataString

## Description
Using selector, sets default load data with string value for the parametric object.
Available selectors : kDLDSelectorGroupName = 2, kDLDSelectorLoadID = 3, kDLDSelectorLoadName = 4, kDLDSelectorWeight = 5, kDLDSelectorPrmLoadID = 6, kDLDSelectorPrmName = 7,	kDLDSelectorPrmWeight = 8, kDLDSelPrmTotalDistWght = 9. <br />
Selector kDLDSelectorGroupName determinate the category, where the load will be displayed in the overview. This selector can be used with one of the following values: 'Audio', 'Video', 'Light', 'Decoration' (displayed as Scenery), 'Cable', 'Truss' and 'LoadingPoint'.

```pascal
PROCEDURE DLDSetLoadDataString(
				selector : INTEGER;
				value    : STRING);
```

```python
def vs.DLDSetLoadDataString(selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|value|STRING|   |

## Examples
```pascal
DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude, TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName, 'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName,GetPlugInString(20000));
	DLDSetLoadDataString( kDLDPositionParamName,'Position');
DLDEndLoadData;

DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,	FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude,		TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName,	'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName, 	GetPlugInString(15000));
	DLDSetLoadDataString( kDLDPositionParamName,	'Position');
DLDEndLoadData;

DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude, TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName, 'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName,GetPlugInString(10000));
	DLDSetLoadDataString( kDLDPositionParamName,'Position');
DLDEndLoadData;
```
```python
import vs

# Using selector, sets default load data with string value for the parametric
# object.
selector = 1
value = 'Example'

vs.DLDSetLoadDataString(selector, value)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
