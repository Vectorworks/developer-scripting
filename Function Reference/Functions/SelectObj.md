# SelectObj

## Description
Selects all objects which match the search criteria.

```pascal
PROCEDURE SelectObj(c : CRITERIA);
```

```python
def vs.SelectObj(c):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
[SelectandDelObjects](examples/SelectandDelObjects.md)

```pascal
x := GetPlugInString(5001);
tmpQStr := Concat( '(C = ',QStr(x),')' );
SelectObj(tmpQStr);
IF NumI < OrigNumSelObj THEN
	BEGIN
	NumI := NumI+1;
	polyHandle := SelectionSet[NumI];{(NextSObj2(polyHandle))}

SelectObj((R IN [kInstObjName]));

BEGIN
	DSelectAll;
	SelectObj(INSYMBOL & INVIEWPORT & (R IN [kHoistPIOName]));
END;
```
```python
import vs

# Selects all objects which match the search criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

vs.SelectObj(c)
```
See also in tutorials: [10. Iterate the Drawing and Report a Summary](ai%20examples/10_IterateAndReport.md)

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
