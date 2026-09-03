# IFC_DMSetFieldOpt

```pascal
FUNCTION IFC_DMSetFieldOpt(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING;
				bOptional      : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMSetFieldOpt(inStrObjName, inStrEntryName, inStrFieldName, bOptional):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|bOptional|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMSetFieldOpt('Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'
bOptional = True

ok = vs.IFC_DMSetFieldOpt(inStrObjName, inStrEntryName, inStrFieldName, bOptional)
if ok:
    vs.Message('IFC_DMSetFieldOpt succeeded')
else:
    vs.Message('IFC_DMSetFieldOpt failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
