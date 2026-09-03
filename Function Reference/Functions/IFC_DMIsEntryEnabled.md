# IFC_DMIsEntryEnabled

## Description
Checks if the indicated entry from current IFC Data Mapping is enabled.

```pascal
FUNCTION IFC_DMIsEntryEnabled(
				inStrObjName   : STRING;
				inStrEntryName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsEntryEnabled(inStrObjName, inStrEntryName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMIsEntryEnabled('Example', 'Example');
```
```python
import vs

# Checks if the indicated entry from current IFC Data Mapping is enabled.
inStrObjName = 'Example'
inStrEntryName = 'Example'

ok = vs.IFC_DMIsEntryEnabled(inStrObjName, inStrEntryName)
if ok:
    vs.Message('IFC_DMIsEntryEnabled succeeded')
else:
    vs.Message('IFC_DMIsEntryEnabled failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
