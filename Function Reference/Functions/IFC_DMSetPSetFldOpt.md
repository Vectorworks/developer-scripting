# IFC_DMSetPSetFldOpt

## Description
Sets specified Field for IfcEntry's PSet Optional.

```pascal
FUNCTION IFC_DMSetPSetFldOpt(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				bOptional     : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldOpt(strObjectName, strEntryName, strPSetName, strFieldName, bOptional):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|bOptional|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMSetPSetFldOpt('Example', 'Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

# Sets specified Field for IfcEntry's PSet Optional.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'
bOptional = True

ok = vs.IFC_DMSetPSetFldOpt(strObjectName, strEntryName, strPSetName, strFieldName, bOptional)
if ok:
    vs.Message('IFC_DMSetPSetFldOpt succeeded')
else:
    vs.Message('IFC_DMSetPSetFldOpt failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
