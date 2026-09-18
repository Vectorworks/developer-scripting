# IFC_DelRecFromObjMap

## Description
Deletes Record from Object's mapping.

```pascal
FUNCTION IFC_DelRecFromObjMap(
				objectName : STRING;
				recordName : STRING): BOOLEAN;
```

```python
def vs.IFC_DelRecFromObjMap(objectName, recordName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|recordName|STRING|   |

## Examples
```pascal
resultOK := IFC_DelRecFromObjMap('Example', 'MyRecord');
```
```python
import vs

# Deletes Record from Object's mapping.
objectName = 'Example'
recordName = 'MyRecord'

ok = vs.IFC_DelRecFromObjMap(objectName, recordName)
if ok:
    vs.Message('IFC_DelRecFromObjMap succeeded')
else:
    vs.Message('IFC_DelRecFromObjMap failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
