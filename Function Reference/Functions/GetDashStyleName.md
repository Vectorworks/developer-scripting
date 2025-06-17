# GetDashStyleName

## Description
Retrieves the dash style name of the specified dash style index.

```pascal
FUNCTION GetDashStyleName(DashStyleIndex : INTEGER): STRING;
```

```python
def vs.GetDashStyleName(DashStyleIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|DashStyleIndex|INTEGER|The the index of the dash style.|

## Remarks
*\_c\_*, (2016.03.01):  The dash style index required is relative to the dash style list, not the name list. Use [GetDashStyle](GetDashStyle.md) or [GetDashStyleIndex](GetDashStyleIndex.md) to obtain it. Analogically, the dash style name returned is the name in the dash style list (you set it with [SetDashStyleName](SetDashStyleName.md)), not the name list. This can be diverging.

<code lang="vs">
dashStyleName := GetDashStyleName(GetDashStyleIndex(TRUE, 1, 0.12, 0.03));
{ should return 'ISO-02 Dashed' or its localized name, if a style with these pairs exists
in the active document, otherwise it creates one with a generic name }
```

## See Also
VS Functions:
[SetDashStyleName](SetDashStyleName.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Object Names](../Categories/Object%20Names.md)
