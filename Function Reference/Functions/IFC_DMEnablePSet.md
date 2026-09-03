# IFC_DMEnablePSet

## Description
Enables/Disables indicated Entry's PSet from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMEnablePSet(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				bEnable       : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMEnablePSet(strObjectName, strEntryName, strPSetName, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|bEnable|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMEnablePSet('Example', 'Example', 'Example', TRUE);
```
```python
import vs

# Enables/Disables indicated Entry's PSet from current IFC Data Mapping.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
bEnable = True

ok = vs.IFC_DMEnablePSet(strObjectName, strEntryName, strPSetName, bEnable)
if ok:
    vs.Message('IFC_DMEnablePSet succeeded')
else:
    vs.Message('IFC_DMEnablePSet failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
