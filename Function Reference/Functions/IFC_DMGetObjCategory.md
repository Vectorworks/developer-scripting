# IFC_DMGetObjCategory

## Description
Returns the Category for the Indicated Object.

```pascal
FUNCTION IFC_DMGetObjCategory(
				strObjectName      : STRING;
				outMappingCategory : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetObjCategory(strObjectName):
    return BOOLEAN, outMappingCategory
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|outMappingCategory|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMGetObjCategory('Example', 1);
```
```python
import vs

# Returns the Category for the Indicated Object.
strObjectName = 'Example'

ok = vs.IFC_DMGetObjCategory(strObjectName)
if ok:
    vs.Message('IFC_DMGetObjCategory succeeded')
else:
    vs.Message('IFC_DMGetObjCategory failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
