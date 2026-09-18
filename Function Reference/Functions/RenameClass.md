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

## Examples
```pascal
BEGIN
IF kDebug THEN Writeln ('Renamed : ','New ',NewClass[I,1],' Old ',ExistClass[(ClassMaping[I,1]),1]);
RenameClass(ExistClass[(ClassMaping[I,1]),1],NewClass[I,1]);
{ClassVisi := GetCVis(ExistClass[(ClassMaping[I,1]),1]);
Case ClassVisi of
	0: ShowClass(ExistClass[(ClassMaping[I,1]),1]);
	1:HideClass(ExistClass[(ClassMaping[I,1]),1]);

IF NOT stillUsed THEN RenameClass (oldClass, newClass)
ELSE NameClass (newClass);
```
```python
import vs

# Renames the specified class.
className = 'None'
newName = 'Example'

vs.RenameClass(className, newName)
```

## Version
Availability: from VectorWorks8.5

## Category
* [Classes](../Categories/Classes.md)
