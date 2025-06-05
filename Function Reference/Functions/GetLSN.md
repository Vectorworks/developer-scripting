# GetLSN

## Description
Function GetLSN returns the line style of the referenced object.

```pascal
FUNCTION GetLSN(h : HANDLE): LONGINT;
```

```python
def vs.GetLSN(h):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
*_c_* (2016.02.29): Returns a name list index, while the older routine [[VS:GetLS]] returned a dash style index. 

<code lang="vs">
styleName := Index2Name(-GetLSN(FSActLayer));
{ returns the name of the dash style defintion of the first selected object }
</code>

## See Also
VS Functions:
[SetLSN](SetLSN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
