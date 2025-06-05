# Length

## Description
<b>[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)</b>. See [[VS:LengthN|LengthN]] for a replacement.

Returns the length of an object. If more than one object matches the search criteria, the function will return the sum of all the matching object lengths.

```pascal
FUNCTION Length(c : CRITERIA): REAL;
```

```python
def vs.Length(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
LengthValue:=Length(C='CrossMembers');
{returns the length of all objects in class 'CrossMembers'}
```
#### Python ####
```python

```

## Version
Availability: from All Versions
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
