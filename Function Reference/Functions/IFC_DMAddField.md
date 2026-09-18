# IFC_DMAddField

## Description
Adds a field to current IFC Data Mapping.

```pascal
FUNCTION IFC_DMAddField(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING;
				type           : INTEGER;
				bOptional      : BOOLEAN;
				bEnable        : BOOLEAN;
				bEmpty         : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMAddField(inStrObjName, inStrEntryName, inStrFieldName, type, bOptional, bEnable, bEmpty):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|type|INTEGER|   |
|bOptional|BOOLEAN|   |
|bEnable|BOOLEAN|   |
|bEmpty|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMAddField('Example', 'Example', 'MyRecord', 1, TRUE, FALSE, TRUE);
```
```python
import vs

# Adds a field to current IFC Data Mapping.
inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'
type = 0
bOptional = True
bEnable = True
bEmpty = True

ok = vs.IFC_DMAddField(inStrObjName, inStrEntryName, inStrFieldName, type, bOptional, bEnable, bEmpty)
if ok:
    vs.Message('IFC_DMAddField succeeded')
else:
    vs.Message('IFC_DMAddField failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
