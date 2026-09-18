# IFC_DMSetFieldMap

```pascal
FUNCTION IFC_DMSetFieldMap(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING;
				strMappingSrc  : STRING): BOOLEAN;
```

```python
def vs.IFC_DMSetFieldMap(inStrObjName, inStrEntryName, inStrFieldName, strMappingSrc):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|strMappingSrc|STRING|   |

## Examples
```pascal
resultOK := IFC_DMSetFieldMap('Example', 'Example', 'MyRecord', 'Example');
```
```python
import vs

inStrObjName = 'Example'
inStrEntryName = 'Example'
inStrFieldName = 'MyField'
strMappingSrc = 'Example'

ok = vs.IFC_DMSetFieldMap(inStrObjName, inStrEntryName, inStrFieldName, strMappingSrc)
if ok:
    vs.Message('IFC_DMSetFieldMap succeeded')
else:
    vs.Message('IFC_DMSetFieldMap failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
