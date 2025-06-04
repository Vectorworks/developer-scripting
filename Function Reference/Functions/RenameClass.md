# RenameClass

## Description
Renames the specified class. 

All objects assigned to the class being renamed are updated.

```pascal
PROCEDURE RenameClass(
				className : STRING;
				newName   : STRING);
```

```python
def vs.RenameClass(className, newName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Existing name of the class.|
|newName|STRING|New name for the class.|

## Remarks
It seems that when you try to rename a class to a class name that already exist, VW will create a new class with name, followed with "-2" or in case that the class name ends with a number, the number + 1.

## Version
Availability: from VectorWorks8.5

## Category
* [Classes](../Categories/Classes.md)
