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

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
