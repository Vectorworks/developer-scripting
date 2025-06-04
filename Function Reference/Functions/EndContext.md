# EndContext

## Description
Use this function in conjuction with BeginContext to have VW automatically accept or reject any changes that were made during the Begin/End block.

```pascal
PROCEDURE EndContext(acceptOrReject : INTEGER);
```

```python
def vs.EndContext(acceptOrReject):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acceptOrReject|INTEGER|Specify 0 to reject changes or 1 to accept changes|

## Remarks
If you do not use this construct and you create a temporary plug-in object that itself creates a new class, the new class will remain even after you delete the temporary plug-in object.

## See Also
VS Functions:
[BeginContext](BeginContext.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Utility](../Categories/Utility.md)
