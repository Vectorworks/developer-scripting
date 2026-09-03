# IFC_DMAddPSetForEnt

## Description
Adds new Property Set to specified Object IfcEntry's group in IFC Data Mapping.

```pascal
FUNCTION IFC_DMAddPSetForEnt(
				strObjectName    : STRING;
				strEntryName     : STRING;
				strPSetName      : STRING;
				bEnabled         : BOOLEAN;
				strPSetCondition : STRING): BOOLEAN;
```

```python
def vs.IFC_DMAddPSetForEnt(strObjectName, strEntryName, strPSetName, bEnabled, strPSetCondition):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|bEnabled|BOOLEAN|   |
|strPSetCondition|STRING|   |

## Examples
```pascal
resultOK := IFC_DMAddPSetForEnt('Example', 'Example', 'Example', TRUE, 'Example');
```
```python
import vs

# Adds new Property Set to specified Object IfcEntry's group in IFC Data Mapping.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
bEnabled = True
strPSetCondition = 'Example'

ok = vs.IFC_DMAddPSetForEnt(strObjectName, strEntryName, strPSetName, bEnabled, strPSetCondition)
if ok:
    vs.Message('IFC_DMAddPSetForEnt succeeded')
else:
    vs.Message('IFC_DMAddPSetForEnt failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
