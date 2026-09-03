# IFC_DMSetPSetFldEmpt

## Description
Sets specified Field for IfcEntry's PSet Empty.

```pascal
FUNCTION IFC_DMSetPSetFldEmpt(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				bEmpty        : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldEmpt(strObjectName, strEntryName, strPSetName, strFieldName, bEmpty):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|bEmpty|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMSetPSetFldEmpt('Example', 'Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

# Sets specified Field for IfcEntry's PSet Empty.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'
bEmpty = True

ok = vs.IFC_DMSetPSetFldEmpt(strObjectName, strEntryName, strPSetName, strFieldName, bEmpty)
if ok:
    vs.Message('IFC_DMSetPSetFldEmpt succeeded')
else:
    vs.Message('IFC_DMSetPSetFldEmpt failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
