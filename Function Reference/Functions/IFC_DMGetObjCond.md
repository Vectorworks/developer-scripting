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

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
