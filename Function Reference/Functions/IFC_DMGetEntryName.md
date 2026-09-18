# IFC_DMGetEntryName

## Description
Gets the name of entry for indicated index from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetEntryName(
				index            : INTEGER;
				inStrObjName     : STRING;
				VAR outStrResult : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetEntryName(index, inStrObjName):
    return (BOOLEAN, outStrResult)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|   |
|inStrObjName|STRING|   |
|outStrResult|STRING|   |

## Examples
```pascal
resultOK := IFC_DMGetEntryName(1, 'Example', 'Example');
```
```python
import vs

# Gets the name of entry for indicated index from current IFC Data Mapping.
index = 1
inStrObjName = 'Example'

ok, outStrResult = vs.IFC_DMGetEntryName(index, inStrObjName)
vs.Message('IFC_DMGetEntryName returned: ' + str((ok, outStrResult)))
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
