# IFC_DMDeletePSetFld

## Description
Deletes specified IfcEntry's PSet Field.

```pascal
FUNCTION IFC_DMDeletePSetFld(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING): BOOLEAN;
```

```python
def vs.IFC_DMDeletePSetFld(strObjectName, strEntryName, strPSetName, strFieldName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMDeletePSetFld('Example', 'Example', 'Example', 'MyRecord');
```
```python
import vs

# Deletes specified IfcEntry's PSet Field.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'

ok = vs.IFC_DMDeletePSetFld(strObjectName, strEntryName, strPSetName, strFieldName)
if ok:
    vs.Message('IFC_DMDeletePSetFld succeeded')
else:
    vs.Message('IFC_DMDeletePSetFld failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
