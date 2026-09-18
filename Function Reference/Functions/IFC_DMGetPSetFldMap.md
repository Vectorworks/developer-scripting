# IFC_DMGetPSetFldMap

## Description
Gets the Mapping Source of specified Field for IfcEntry's PSet.

```pascal
FUNCTION IFC_DMGetPSetFldMap(
				strObjectName        : STRING;
				strEntryName         : STRING;
				strPSetName          : STRING;
				strFieldName         : STRING;
				VAR outStrMappingSrc : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetFldMap(strObjectName, strEntryName, strPSetName, strFieldName):
    return (BOOLEAN, outStrMappingSrc)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|outStrMappingSrc|STRING|   |

## Examples
```pascal
resultOK := IFC_DMGetPSetFldMap('Example', 'Example', 'Example', 'MyRecord', 'Example');
```
```python
import vs

# Gets the Mapping Source of specified Field for IfcEntry's PSet.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'

ok, outStrMappingSrc = vs.IFC_DMGetPSetFldMap(strObjectName, strEntryName, strPSetName, strFieldName)
vs.Message('IFC_DMGetPSetFldMap returned: ' + str((ok, outStrMappingSrc)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
