# IFC_DMSetObjectCond

## Description
Sets the Condition for specified Object.

```pascal
FUNCTION IFC_DMSetObjectCond(
				strObjectName : STRING;
				strCondition  : STRING): BOOLEAN;
```

```python
def vs.IFC_DMSetObjectCond(strObjectName, strCondition):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strCondition|STRING|   |

## Examples
```pascal
resultOK := IFC_DMSetObjectCond('Example', 'Example');
```
```python
import vs

# Sets the Condition for specified Object.
strObjectName = 'Example'
strCondition = 'Example'

ok = vs.IFC_DMSetObjectCond(strObjectName, strCondition)
if ok:
    vs.Message('IFC_DMSetObjectCond succeeded')
else:
    vs.Message('IFC_DMSetObjectCond failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
