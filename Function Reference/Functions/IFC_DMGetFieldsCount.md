# IFC_DMGetFieldsCount

## Description
Gets fields count for indicated entry from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetFieldsCount(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				VAR outCount   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetFieldsCount(inStrObjName, inStrEntryName):
    return (BOOLEAN, outCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|outCount|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMGetFieldsCount('Example', 'Example', 1);
```
```python
import vs

# Gets fields count for indicated entry from current IFC Data Mapping.
inStrObjName = 'Example'
inStrEntryName = 'Example'

ok, outCount = vs.IFC_DMGetFieldsCount(inStrObjName, inStrEntryName)
vs.Message('IFC_DMGetFieldsCount returned: ' + str((ok, outCount)))
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
