# SetLSN

## Description
Procedure SetLSN sets the linestyle of the referenced object.

If the value is in the range 0 to 71, the specified fill pattern is applied as the linestyle; a negative value will apply the line type resource whose internal index is the negative of the value.

```pascal
PROCEDURE SetLSN(
				h  : HANDLE;
				ls : LONGINT);
```

```python
def vs.SetLSN(h, ls):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|ls|LONGINT|Linestyle to apply to object.|

## Remarks
([[User:CBM-c-|_c_]] 2016.02.29): Expects a name list index, while the older routine [[VS:GetLS]] expected a dash style index. 

<code lang="vs">
IF GetObject('ISO-02 Dashed') <> NIL THEN
	SetLSN(FSActLayer, -Name2Index('ISO-02 Dashed')); { sets the first selected object to 'ISO-02 Dashed' if the style is present }
</code>

## See Also
VS Functions:
[GetLSN](GetLSN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
