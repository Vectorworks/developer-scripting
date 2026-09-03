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

## Examples
```pascal
END;
IF (ok) & (linestyleDo) & (linestyleVa <> mT) THEN BEGIN
	if not ObjectHasLS(h) then ok := false else BEGIN
		IF IsLSByClass(h)
			THEN num1 := GetClLSN(GetClass(h))
			ELSE num1 := GetLSN(h);
		num2 := Str2Num(linestyleVa);
		ok := (ok) & (((linestyleOp = '=' ) & (num1 =  num2)) |
		              ((linestyleOp = '<' ) & (num1 <  num2)) |
		              ((linestyleOp = '>' ) & (num1 >  num2)) |

SetLSN( h4, GetClLSN( kModifierClass ) );
SetLW( h4, GetClLW( kModifierClass ) );

IF GetClLSN (UserClassName) <> TmpClassInfo.LS THEN SetClLSN (UserClassName, TmpClassInfo.LS);
```
```python
import vs

# Returns the line style of the specified class.
className = 'None'

resultN = vs.GetClLSN(className)
vs.Message('GetClLSN returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetClLSN](SetClLSN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Classes](../Categories/Classes.md)
