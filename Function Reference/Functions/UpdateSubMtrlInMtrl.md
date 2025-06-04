# UpdateSubMtrlInMtrl

## Description
Updates a Simple material which is a part of a Compound material. Sets new values for its fraction and whether it should be the primary material. Fraction can have value between 0.0 and 1.0. &quot;Primary&quot; material is a simple material which carries the graphical attributes to be used by the compound material.

```pascal
FUNCTION UpdateSubMtrlInMtrl(
				hMaterial   : HANDLE;
				subMtrlName : STRING;
				fraction    : REAL;
				makePrimary : BOOLEAN): Boolean;
```

```python
def vs.UpdateSubMtrlInMtrl(hMaterial, subMtrlName, fraction, makePrimary):
    return Boolean
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hMaterial|HANDLE|Handle of a Compound material|
|subMtrlName|STRING|Name of a Simple material to be updated|
|fraction|REAL|Fraction of the Simple material|
|makePrimary|BOOLEAN|True if this Simple material should become the primary material of the Compound material|

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
