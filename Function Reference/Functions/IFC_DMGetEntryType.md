# IFC_DMGetEntryType

## Description
Returns the IfcEntity type for specified Object in IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetEntryType(
				strObjectName : STRING;
				index         : INTEGER;
				VAR outType   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetEntryType(strObjectName, index):
    return (BOOLEAN, outType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|index|INTEGER|   |
|outType|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMGetEntryType('Example', 1, 2);
```
```python
import vs

# Returns the IfcEntity type for specified Object in IFC Data Mapping.
strObjectName = 'Example'
index = 1

ok, outType = vs.IFC_DMGetEntryType(strObjectName, index)
vs.Message('IFC_DMGetEntryType returned: ' + str((ok, outType)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
