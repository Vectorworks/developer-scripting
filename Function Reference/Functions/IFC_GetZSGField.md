# IFC_GetZSGField

## Description
Gets Zone, System or Group field value.

```pascal
FUNCTION IFC_GetZSGField(
				selector          : INTEGER;
				VAR ZSGName       : STRING;
				fieldName         : STRING;
				VAR outFieldValue : STRING): BOOLEAN;
```

```python
def vs.IFC_GetZSGField(selector, fieldName):
    return (BOOLEAN, ZSGName, outFieldValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|ZSGName|STRING|   |
|fieldName|STRING|   |
|outFieldValue|STRING|   |

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
