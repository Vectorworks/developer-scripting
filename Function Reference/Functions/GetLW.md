# GetLW

## Description
Function GetLW returns the line weight of the referenced object. The value returned represents the width in mils.

```pascal
FUNCTION GetLW(h : HANDLE): INTEGER;
```

```python
def vs.GetLW(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Criteria searching by lineweight works differently. An object with a lineweight by class can be found with this: 
<code>SelectObj((LW&lt;.0000000000002));</code>
Then you can use GetLW to determine the actual lineweight.

[[User:Orso.b.schmid| orso]]: (1 mil = 1/1000 in)

## Examples
==== VectorScript ====
```pascal
PROCEDURE GetLWExample;
VAR
    x, y : REAL;
    h : HANDLE;
BEGIN
    GetPt(x, y);
    h := PickObject(x, y);

    IF h <> NIL THEN
        Message(GetLW(h));
END;
RUN(GetLWExample);
```
==== Python ====
```python
def PickPointCallback(pt):
	h = vs.PickObject(pt[0], pt[1])
	if h != None:
		vs.Message(vs.GetLW(h))
	

def GetLWExample():
	vs.GetPt( PickPointCallback )
    
GetLWExample()
```

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
