# IFC_DMIsPSetFldOpt

## Description
Checks if specified Field for IfcEntry's PSet is Optional.

```pascal
FUNCTION IFC_DMIsPSetFldOpt(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsPSetFldOpt(strObjectName, strEntryName, strPSetName, strFieldName):
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
resultOK := IFC_DMIsPSetFldOpt('Example', 'Example', 'Example', 'MyRecord');
```
```python
import vs

# Checks if specified Field for IfcEntry's PSet is Optional.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'

ok = vs.IFC_DMIsPSetFldOpt(strObjectName, strEntryName, strPSetName, strFieldName)
if ok:
    vs.Message('IFC_DMIsPSetFldOpt succeeded')
else:
    vs.Message('IFC_DMIsPSetFldOpt failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
