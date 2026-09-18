# ReleaseObj

## Description
Releases all objects which match the search criteria.

```pascal
PROCEDURE ReleaseObj(c : CRITERIA);
```

```python
def vs.ReleaseObj(c):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria|

## Examples
```pascal
ReleaseObj(c);
```
```python
import vs

# Releases all objects which match the search criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

vs.ReleaseObj(c)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Criteria](../Categories/Criteria.md)
