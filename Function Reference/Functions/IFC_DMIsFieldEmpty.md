# IFC_DMIsFieldEmpty

```pascal
FUNCTION IFC_DMIsFieldEmpty(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsFieldEmpty(inStrObjName, inStrEntryName, inStrFieldName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMIsFieldEmpty('Example', 'Example', 'MyRecord');
```
```python
import vs

inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'

ok = vs.IFC_DMIsFieldEmpty(inStrObjName, inStrEntryName, inStrFieldName)
if ok:
    vs.Message('IFC_DMIsFieldEmpty succeeded')
else:
    vs.Message('IFC_DMIsFieldEmpty failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
