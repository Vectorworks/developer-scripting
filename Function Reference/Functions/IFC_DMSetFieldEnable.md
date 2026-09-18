# IFC_DMSetFieldEnable

```pascal
FUNCTION IFC_DMSetFieldEnable(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING;
				bEnable        : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMSetFieldEnable(inStrObjName, inStrEntryName, inStrFieldName, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|bEnable|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMSetFieldEnable('Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'
bEnable = True

ok = vs.IFC_DMSetFieldEnable(inStrObjName, inStrEntryName, inStrFieldName, bEnable)
if ok:
    vs.Message('IFC_DMSetFieldEnable succeeded')
else:
    vs.Message('IFC_DMSetFieldEnable failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
