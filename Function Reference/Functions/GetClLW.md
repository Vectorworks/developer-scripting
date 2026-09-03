# GetClLW

## Description
Returns the line weight of the specified class.

```pascal
FUNCTION GetClLW(className : STRING): INTEGER;
```

```python
def vs.GetClLW(className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
Returns the line weight of the class named className.

## Examples
#### VectorScript ####
```pascal
pbLineWt:= GetClLW('Property Bounds');
```
#### Python ####
```python
pbLineWt = vs.GetClLW('Property Bounds')
```

```pascal
SetLSN( h4, GetClLSN( kModifierClass ) );
SetLW( h4, GetClLW( kModifierClass ) );

IF GetClLW (UserClassName) <> TmpClassInfo.LW THEN SetClLW (UserClassName, TmpClassInfo.LW);

IF GetClLW (UserClassName) <> TmpClassInfo.LW THEN
BEGIN
	gClassList [classIndex].LW := GetClLW (UserClassName);
	WriteToClassWS (classIndex, 2, GetClLW (UserClassName), '');
END;
```
```python
import vs

# Returns the line weight of the specified class.
className = 'None'

resultN = vs.GetClLW(className)
vs.Message('GetClLW returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
