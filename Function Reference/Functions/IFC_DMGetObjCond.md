# IFC_DMGetObjCond

## Description
Returns the Condition for specified Object in IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetObjCond(
				strObjectName             : STRING;
				VAR outStrObjectCondition : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetObjCond(strObjectName):
    return (BOOLEAN, outStrObjectCondition)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|outStrObjectCondition|STRING|   |

## Examples
```pascal
resultOK := IFC_DMGetObjCond('Example', 'Example');
```
```python
import vs

# Returns the Condition for specified Object in IFC Data Mapping.
strObjectName = 'Example'

ok, outStrObjectCondition = vs.IFC_DMGetObjCond(strObjectName)
vs.Message('IFC_DMGetObjCond returned: ' + str((ok, outStrObjectCondition)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
