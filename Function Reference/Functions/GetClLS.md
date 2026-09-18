# GetClLS

## Description
Returns the line style of the specified class.

```pascal
FUNCTION GetClLS(className : STRING): INTEGER;
```

```python
def vs.GetClLS(className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
Returns the line style of the class named className.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
Message(GetClLS('Property Bounds'));
END;
RUN(Example);
```
#### Python ####
#### Python ####
```python
def	Example():
	vs.Message(vs.GetClLS('Property Bounds'))
Example()
```

```pascal
resultN := GetClLS('Wall');
```
```python
import vs

# Returns the line style of the specified class.
className = 'None'

resultN = vs.GetClLS(className)
vs.Message('GetClLS returned: ' + str(resultN))
```

## See Also
[GetClLSN](GetClLSN.md), [SetClLSN](SetClLSN.md) from Vectorworks 2013
[SetClLS](SetClLS.md)

## Version
Availability: from VectorWorks 8.0, Deprecated from Vectorworks 2013

## Category
* [Classes](../Categories/Classes.md)
