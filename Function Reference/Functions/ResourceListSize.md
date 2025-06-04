# ResourceListSize

## Description
Returns the number of items in the specified resource list.

```pascal
FUNCTION ResourceListSize(listID : LONGINT): LONGINT;
```

```python
def vs.ResourceListSize(listID):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resouce list created by the BuildResourceList function.|

## Examples
#### VectorScript ####
```pascal
{ Update numItems as the number of items in the resource list has }
{ changed. }
numItems := ResourceListSize(listID);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
