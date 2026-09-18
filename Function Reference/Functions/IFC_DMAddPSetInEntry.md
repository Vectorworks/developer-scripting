# IFC_DMAddPSetInEntry

## Description
Adds a Pset to indicated object's entry from current Data Mapping.

```pascal
FUNCTION IFC_DMAddPSetInEntry(
				inStrObjName       : STRING;
				inStrEntryName     : STRING;
				inStrPsetName      : STRING;
				bEnable            : BOOLEAN;
				inStrPsetCondition : STRING): BOOLEAN;
```

```python
def vs.IFC_DMAddPSetInEntry(inStrObjName, inStrEntryName, inStrPsetName, bEnable, inStrPsetCondition):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrPsetName|STRING|   |
|bEnable|BOOLEAN|   |
|inStrPsetCondition|STRING|   |

## Examples
```pascal
resultOK := IFC_DMAddPSetInEntry('Example', 'Example', 'Example', TRUE, 'Example');
```
```python
import vs

# Adds a Pset to indicated object's entry from current Data Mapping.
inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrPsetName = 'Example'
bEnable = True
inStrPsetCondition = 'Example'

ok = vs.IFC_DMAddPSetInEntry(inStrObjName, inStrEntryName, inStrPsetName, bEnable, inStrPsetCondition)
if ok:
    vs.Message('IFC_DMAddPSetInEntry succeeded')
else:
    vs.Message('IFC_DMAddPSetInEntry failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
