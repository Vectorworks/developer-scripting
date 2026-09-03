# CheckoutObj

## Description
Checkouts all objects which match the search criteria.

```pascal
PROCEDURE CheckoutObj(c : CRITERIA);
```

```python
def vs.CheckoutObj(c):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria|

## Examples
```pascal
CheckoutObj(c);
```
```python
import vs

# Checkouts all objects which match the search criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

vs.CheckoutObj(c)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Criteria](../Categories/Criteria.md)
