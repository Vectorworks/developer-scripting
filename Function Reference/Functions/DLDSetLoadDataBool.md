# DLDSetLoadDataBool

## Description
Using selector, sets default load data with boolean value for the parametric object.
Available selectors : kDLDSelectorInclude = 1, kDLDSelHandlePosTransf = 10.

```pascal
PROCEDURE DLDSetLoadDataBool(
				selector : INTEGER;
				value    : BOOLEAN);
```

```python
def vs.DLDSetLoadDataBool(selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|value|BOOLEAN|   |

## Examples
```pascal
DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude, TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName, 'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName,GetPlugInString(20000));
	DLDSetLoadDataString( kDLDPositionParamName,'Position');

DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,	FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude,		TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName,	'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName, 	GetPlugInString(15000));
	DLDSetLoadDataString( kDLDPositionParamName,	'Position');

DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude, TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName, 'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName,GetPlugInString(10000));
	DLDSetLoadDataString( kDLDPositionParamName,'Position');
```
```python
import vs

# Using selector, sets default load data with boolean value for the
# parametric object.
selector = 1
value = True

vs.DLDSetLoadDataBool(selector, value)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
