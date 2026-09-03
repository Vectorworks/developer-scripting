# IFC_DMSetFieldEmpty

```pascal
FUNCTION IFC_DMSetFieldEmpty(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING;
				bEmpty         : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMSetFieldEmpty(inStrObjName, inStrEntryName, inStrFieldName, bEmpty):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|bEmpty|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMSetFieldEmpty('Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'
bEmpty = True

ok = vs.IFC_DMSetFieldEmpty(inStrObjName, inStrEntryName, inStrFieldName, bEmpty)
if ok:
    vs.Message('IFC_DMSetFieldEmpty succeeded')
else:
    vs.Message('IFC_DMSetFieldEmpty failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
