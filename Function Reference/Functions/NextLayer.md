# NextLayer

## Description
Function NextLayer returns a handle to the next layer in the document after the referenced. If the end of the list has been reached, the function returns NIL.

```pascal
FUNCTION NextLayer(h : HANDLE): HANDLE;
```

```python
def vs.NextLayer(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Examples
[TraverseObjects](examples/TraverseObjects.md)

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
