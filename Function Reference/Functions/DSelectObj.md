# DSelectObj

## Description
Deselects all objects which match the search criteria.

```pascal
PROCEDURE DSelectObj(c : CRITERIA);
```

```python
def vs.DSelectObj(c):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
DSelectObj(S='Pine Tree');
{deselects all 'Pine Tree' symbols}
```
#### Python ####
```python

```

```pascal
BEGIN
	CASE gLayerMode OF
		0:	DSelectAll;	{Active Layer only}
		1,2:DSelectObj(kALL);	{Visible layers/All layers}
		END; {of CASE}
	gObjOption := 0;	{look in all objects}
	END;
```
```python
vs.DSelectObj(c)
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
