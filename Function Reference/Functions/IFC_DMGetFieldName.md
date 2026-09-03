# IFC_DMGetFieldName

## Description
Gets indicated field name from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetFieldName(
				inStrObjName        : STRING;
				inStrEntryName      : STRING;
				index               : INTEGER;
				VAR outStrFieldName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetFieldName(inStrObjName, inStrEntryName, index):
    return (BOOLEAN, outStrFieldName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|index|INTEGER|   |
|outStrFieldName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMGetFieldName('Example', 'Example', 1, 'MyRecord');
```
```python
import vs

# Gets indicated field name from current IFC Data Mapping.
inStrObjName = 'Example'
inStrEntryName = 'Example'
index = 1

ok, outStrFieldName = vs.IFC_DMGetFieldName(inStrObjName, inStrEntryName, index)
vs.Message('IFC_DMGetFieldName returned: ' + str((ok, outStrFieldName)))
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
