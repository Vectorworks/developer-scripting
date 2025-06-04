# ClassList

## Description
Returns the name of the specified class in the document class list. For example,  ClassList(4) will return the name of the fourth class in the list.

```pascal
FUNCTION ClassList(index : LONGINT): STRING;
```

```python
def vs.ClassList(index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|LONGINT|Index of class in class list (range of 1- n).|

## Remarks
NOTE: the manual has said that ClassLIst(4) returns the 4th class in the list, but it actually was returning the 5th class.  BF changed the function on 3/98 so it does return the 4th class.


What is the internal sort order of the class list.  We should add to documentation what the sorting criteria is.

Answer: There's no sorting criteria, the list shows the class in order of their creation. the first created as first, the last created as last.

[[User:CBM-c-|_c_]] [2011.03.29]: If you wish the classes alpha-sorted, you can use [[VS:BuildResourceList| BuildResourceList]].

## Examples
#### VectorScript ####
```pascal
noneClass := ClassList(1); { always returns the 'none' class, unregarded the localization }
dimensionClass := ClassList(2); { always returns the 'dimension' class, unregarded the localization }
classNumber3 := ClassList(3);
classNumber4 := ClassList(4);
```
#### Python ####
```python
noneClass = vs.ClassList(1)
dimensionClass = vs.ClassList(2)
```

## See Also
VS Functions:
[ClassNum](ClassNum.md)

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
