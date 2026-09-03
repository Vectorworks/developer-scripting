# IFC_DMGetFieldMap

## Description
Gets indicated field mapping source from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetFieldMap(
				inStrObjName     : STRING;
				inStrEntryName   : STRING;
				inStrFieldName   : STRING;
				VAR outStrResult : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetFieldMap(inStrObjName, inStrEntryName, inStrFieldName):
    return (BOOLEAN, outStrResult)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|outStrResult|STRING|   |

## Examples
```pascal
resultOK := IFC_DMGetFieldMap('Example', 'Example', 'MyRecord', 'Example');
```
```python
import vs

# Gets indicated field mapping source from current IFC Data Mapping.
inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'

ok, outStrResult = vs.IFC_DMGetFieldMap(inStrObjName, inStrEntryName, inStrFieldName)
vs.Message('IFC_DMGetFieldMap returned: ' + str((ok, outStrResult)))
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
