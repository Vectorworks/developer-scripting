# GetClFPat

## Description
Returns the fill or hatch pattern of the specified class. 

A positive return value in a range of 0 to 71 is the index of the bitmap fill pattern of the class. A negative value is the negative of the fill pattern index (index * -1).

Fill patterns and their associated constants can be found in the [[VS:Function Reference Appendix#Fill Patterns|Function Reference Appendix]].

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

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
