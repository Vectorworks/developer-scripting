# GetClLSN

## Description
Returns the line style of the specified class.<BR>

```pascal
FUNCTION GetClLSN(className : STRING): LONGINT;
```

```python
def vs.GetClLSN(className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
*\_c\_* (2016.02.29): Returns a name list index, while the older routine [GetClLS](GetClLS.md) returned a dash style index. 

```pascal
indx := GetClLSN('None');
IF indx < 0 THEN { if the index is positive then is a pattern. Patterns are not named resources }
	Message(Index2Name(-indx)); { returns the name of the dash style attached to the class 'None', if any }
```

## See Also
VS Functions:
[SetClLSN](SetClLSN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Classes](../Categories/Classes.md)
