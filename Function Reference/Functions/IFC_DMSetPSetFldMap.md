# IFC_DMSetPSetFldMap

## Description
Sets the Mapping Source of specified Field for IfcEntry's PSet.

```pascal
FUNCTION IFC_DMSetPSetFldMap(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				strMappingSrc : STRING): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldMap(strObjectName, strEntryName, strPSetName, strFieldName, strMappingSrc):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|strMappingSrc|STRING|   |

## Examples
```pascal
resultOK := IFC_DMSetPSetFldMap('Example', 'Example', 'Example', 'MyRecord', 'Example');
```
```python
import vs

# Sets the Mapping Source of specified Field for IfcEntry's PSet.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'
strMappingSrc = 'Example'

ok = vs.IFC_DMSetPSetFldMap(strObjectName, strEntryName, strPSetName, strFieldName, strMappingSrc)
if ok:
    vs.Message('IFC_DMSetPSetFldMap succeeded')
else:
    vs.Message('IFC_DMSetPSetFldMap failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
