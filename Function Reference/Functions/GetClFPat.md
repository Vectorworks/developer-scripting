# GetClFPat

## Description
Returns the fill or hatch pattern of the specified class. 

A positive return value in a range of 0 to 71 is the index of the bitmap fill pattern of the class. A negative value is the negative of the fill pattern index (index * -1).

Fill patterns and their associated constants can be found in the [Sciprt Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
FUNCTION GetClFPat(className : STRING): LONGINT;
```

```python
def vs.GetClFPat(className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
Returns the fill pattern of the class named className.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
Message(GetClFPat('Dimension'));
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	vs.Message(vs.GetClFPat('Dimension'));
Example();
```

```pascal
IF GetClFPat (UserClassName) <> TmpClassInfo.FillPat THEN SetClFPat (UserClassName, TmpClassInfo.FillPat);

IF GetClFPat (UserClassName) <> TmpClassInfo.FillPat THEN
BEGIN
	gClassList [classIndex].FillPat := GetClFPat (UserClassName);
	WriteToClassWS (classIndex, 4, GetClFPat (UserClassName), '');
END;

IF GetClLSN (className) <> gClassList [i].LS THEN SetClLSN (className, gClassList [i].LS);
IF GetClLW (className) <> gClassList [i].LW THEN SetClLW (className, gClassList [i].LW);
IF GetClFPat (className) <> gClassList [i].FillPat THEN SetClFPat (className, gClassList [i].FillPat);
```
```python
import vs

# Returns the fill or hatch pattern of the specified class.
className = 'None'

resultN = vs.GetClFPat(className)
vs.Message('GetClFPat returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
