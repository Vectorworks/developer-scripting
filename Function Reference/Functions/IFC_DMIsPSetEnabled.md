# IFC_DMIsPSetEnabled

## Description
Check if a PSet for specified Object's IfcEntry is Enabled.

```pascal
FUNCTION IFC_DMIsPSetEnabled(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsPSetEnabled(strObjectName, strEntryName, strPSetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMIsPSetEnabled('Example', 'Example', 'Example');
```
```python
import vs

# Check if a PSet for specified Object's IfcEntry is Enabled.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'

ok = vs.IFC_DMIsPSetEnabled(strObjectName, strEntryName, strPSetName)
if ok:
    vs.Message('IFC_DMIsPSetEnabled succeeded')
else:
    vs.Message('IFC_DMIsPSetEnabled failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
