# IFC_GetPsetProp2

## Description
Gets the property value, its type and if the value comes from mapping or by instance.

```pascal
FUNCTION IFC_GetPsetProp2(
				hObject          : HANDLE;
				pSetName         : STRING;
				propertyName     : STRING;
				VAR outPropValue : STRING;
				VAR outType      : INTEGER;
				VAR outMap       : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetPsetProp2(hObject, pSetName, propertyName):
    return (BOOLEAN, outPropValue, outType, outMap)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|pSetName|STRING|   |
|propertyName|STRING|   |
|outPropValue|STRING|   |
|outType|INTEGER|   |
|outMap|INTEGER|   |

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
