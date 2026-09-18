# IFC_DMAddEntry

## Description
Adds an entry to indicated object from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMAddEntry(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				bEnable        : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMAddEntry(inStrObjName, inStrEntryName, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|bEnable|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMAddEntry('Example', 'Example', TRUE);
```
```python
import vs

# Adds an entry to indicated object from current IFC Data Mapping.
inStrObjName = 'Example'
inStrEntryName = 'Example'
bEnable = True

ok = vs.IFC_DMAddEntry(inStrObjName, inStrEntryName, bEnable)
if ok:
    vs.Message('IFC_DMAddEntry succeeded')
else:
    vs.Message('IFC_DMAddEntry failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
