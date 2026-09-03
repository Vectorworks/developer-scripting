# IFC_DMSetFieldType

```pascal
FUNCTION IFC_DMSetFieldType(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING;
				type           : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMSetFieldType(inStrObjName, inStrEntryName, inStrFieldName, type):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|type|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMSetFieldType('Example', 'Example', 'MyRecord', 1);
```
```python
import vs

inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'
type = 0

ok = vs.IFC_DMSetFieldType(inStrObjName, inStrEntryName, inStrFieldName, type)
if ok:
    vs.Message('IFC_DMSetFieldType succeeded')
else:
    vs.Message('IFC_DMSetFieldType failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
