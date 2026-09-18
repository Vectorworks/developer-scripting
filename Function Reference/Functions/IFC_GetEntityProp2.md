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

## Examples
```pascal
resultOK := IFC_GetEntityProp2(hObject, 'Example', 'Example', 1, 2);
```
```python
import vs

# Gets the property value, its type and if the value comes from mapping or by
# instance.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
propertyName = 'Example'

ok, outPropValue, outType, outMap = vs.IFC_GetEntityProp2(hObject, propertyName)
vs.Message('IFC_GetEntityProp2 returned: ' + str((ok, outPropValue, outType, outMap)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
