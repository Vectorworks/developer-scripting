# IFC_DMIsFieldOpt

```pascal
FUNCTION IFC_DMIsFieldOpt(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsFieldOpt(inStrObjName, inStrEntryName, inStrFieldName):
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
resultOK := IFC_DMIsFieldOpt('Example', 'Example', 'MyRecord');
```
```python
import vs

inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'

ok = vs.IFC_DMIsFieldOpt(inStrObjName, inStrEntryName, inStrFieldName)
if ok:
    vs.Message('IFC_DMIsFieldOpt succeeded')
else:
    vs.Message('IFC_DMIsFieldOpt failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
