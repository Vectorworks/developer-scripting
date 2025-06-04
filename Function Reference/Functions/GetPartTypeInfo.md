# GetPartTypeInfo

## Description
Get all part information for the specified sub-object. The sub-object must be an object that was tagged as a part.

```pascal
FUNCTION GetPartTypeInfo(
				objectHandle           : HANDLE;
				VAR partTypeName       : STRING;
				VAR dataID             : LONGINT;
				VAR uniqueInstanceName : STRING): BOOLEAN;
```

```python
def vs.GetPartTypeInfo(objectHandle):
    return (BOOLEAN, partTypeName, dataID, uniqueInstanceName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The sub-object handle.|
|partTypeName|STRING|The name of the part type.|
|dataID|LONGINT|The numeric value assigned to this part instance|
|uniqueInstanceName|STRING|The unique name assigned to this part instance.|

## See Also
VS Functions:
[TagSubObjectAsPart](TagSubObjectAsPart.md) 
| [IsObjectTaggedAsPart](IsObjectTaggedAsPart.md) 
| [GetPartTypeName](GetPartTypeName.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
