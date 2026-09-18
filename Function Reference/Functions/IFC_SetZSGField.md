# IFC_SetZSGField

## Description
Sets Zone, System or Group field value.

```pascal
FUNCTION IFC_SetZSGField(
				selector   : INTEGER;
				ZSGName    : STRING;
				fieldName  : STRING;
				fieldValue : STRING): BOOLEAN;
```

```python
def vs.IFC_SetZSGField(selector, ZSGName, fieldName, fieldValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|ZSGName|STRING|   |
|fieldName|STRING|   |
|fieldValue|STRING|   |

## Examples
```pascal
resultOK := IFC_SetZSGField(1, 'Example', 'MyRecord', 'MyRecord');
```
```python
import vs

# Sets Zone, System or Group field value.
selector = 1
ZSGName = 'Example'
fieldName = 'MyField'
fieldValue = 'MyField'

ok = vs.IFC_SetZSGField(selector, ZSGName, fieldName, fieldValue)
if ok:
    vs.Message('IFC_SetZSGField succeeded')
else:
    vs.Message('IFC_SetZSGField failed')
```

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
