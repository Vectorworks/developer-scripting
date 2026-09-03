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

## Examples
```pascal
resultOK := IFC_GetZSGField(1, 'Example', 'MyRecord', 'MyRecord');
```
```python
import vs

# Gets Zone, System or Group field value.
selector = 1
fieldName = 'MyField'

ok, ZSGName, outFieldValue = vs.IFC_GetZSGField(selector, fieldName)
vs.Message('IFC_GetZSGField returned: ' + str((ok, ZSGName, outFieldValue)))
```

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
