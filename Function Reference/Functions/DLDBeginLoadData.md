# DLDBeginLoadData

## Description
Begin creation of load data from that type. 
kDLDTypePointLoad = 1, kDLDTypeDestributedLoad	= 2

```pascal
PROCEDURE DLDBeginLoadData(loadDataType : INTEGER);
```

```python
def vs.DLDBeginLoadData(loadDataType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|loadDataType|INTEGER|   |

## Examples
```pascal
DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude, TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName, 'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName,GetPlugInString(20000));

DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,	FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude,		TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName,	'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName, 	GetPlugInString(15000));

DLDBeginLoadData( kDLDTypePointLoad );
	DLDSetLoadDataBool	( kDLDEnableWeightWidget,FALSE);
	DLDSetLoadDataBool	( kDLDSelectorInclude, TRUE );
	DLDSetLoadDataString( kDLDSelectorGroupName, 'Audio' );
	DLDSetLoadDataString( kDLDSelectorLoadName,GetPlugInString(10000));
```
```python
import vs

# Begin creation of load data from that type.
loadDataType = 0

vs.DLDBeginLoadData(loadDataType)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
