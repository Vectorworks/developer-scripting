# DelClass

## Description
Deletes the specified class from the active document. If there are objects in the class to be deleted, they are reassigned to the None class.

```pascal
PROCEDURE DelClass(className : STRING);
```

```python
def vs.DelClass(className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class to delete.|

## Examples
#### VectorScript ####
```pascal
DelClass('Future Construction');
```
#### Python ####
```python
vs.DelClass('Future Construction')
```

```pascal
BEGIN
IF KDebug THEN Writeln('Deleting Class ',ClassList(I));
DelClass(ClassList(I));
END

{* If any new classes have been added, delete them. *}
IF ClassNum > numExistClasses THEN
	FOR i := ClassNum DOWNTO numExistClasses+1 DO
		DelClass (ClassList (i));

IF NOT stillUsed THEN DelClass (oldClass);
NameClass (newClass);
```
```python
import vs

# Deletes the specified class from the active document.
className = 'None'

vs.DelClass(className)
```

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
