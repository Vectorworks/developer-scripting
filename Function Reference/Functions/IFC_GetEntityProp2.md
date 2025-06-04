# IFC_GetEntityProp2

## Description
Gets the property value, its type and if the value comes from mapping or by instance.

```pascal
FUNCTION IFC_GetEntityProp2(
				hObject          : HANDLE;
				propertyName     : STRING;
				VAR outPropValue : STRING;
				VAR outType      : INTEGER;
				VAR outMap       : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetEntityProp2(hObject, propertyName):
    return (BOOLEAN, outPropValue, outType, outMap)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|propertyName|STRING|   |
|outPropValue|STRING|   |
|outType|INTEGER|   |
|outMap|INTEGER|   |

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
