# IFC_DMDeleteField

## Description
Deletes a field from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMDeleteField(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMDeleteField(inStrObjName, inStrEntryName, inStrFieldName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMDeleteField('Example', 'Example', 'MyRecord');
```
```python
import vs

# Deletes a field from current IFC Data Mapping.
inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'

ok = vs.IFC_DMDeleteField(inStrObjName, inStrEntryName, inStrFieldName)
if ok:
    vs.Message('IFC_DMDeleteField succeeded')
else:
    vs.Message('IFC_DMDeleteField failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
