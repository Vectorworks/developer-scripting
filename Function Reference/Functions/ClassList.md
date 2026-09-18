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

*\_c\_* [2011.03.29]: If you wish the classes alpha-sorted, you can use [BuildResourceList](BuildResourceList.md).

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

```pascal
ALLOCATE classListN [1..ClassNum];
FOR i := 1 TO ClassNum DO
	classListN [i] := ClassList (i);
SortArray(classListN, ClassNum, 0);

BEGIN
	{Empty string means container class}
	kRealNoneClass := ClassList(1);
	IF pShaft_Finish = kRealNoneClass THEN
		SetRField (h, gPluginName, 'Shaft Finish','');
	IF pCapital_Finish = kRealNoneClass THEN
		SetRField (h, gPluginName, 'Capital Finish','');

ALLOCATE classNames [1..ClassNum];
FOR i := 1 TO ClassNum DO
	classNames [i] := ClassList (i);
SortArray (classNames, ClassNum, 0);
```
```python
import vs

# Returns the name of the specified class in the document class list.
index = 1

text = vs.ClassList(index)
vs.Message('ClassList returned: ' + str(text))
```

## See Also
VS Functions:
[ClassNum](ClassNum.md)

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
