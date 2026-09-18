# IFC_DMIsFieldEnabled

```pascal
FUNCTION IFC_DMIsFieldEnabled(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsFieldEnabled(inStrObjName, inStrEntryName, inStrFieldName):
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
resultOK := IFC_DMIsFieldEnabled('Example', 'Example', 'MyRecord');
```
```python
import vs

inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'

ok = vs.IFC_DMIsFieldEnabled(inStrObjName, inStrEntryName, inStrFieldName)
if ok:
    vs.Message('IFC_DMIsFieldEnabled succeeded')
else:
    vs.Message('IFC_DMIsFieldEnabled failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
