# SlabFromPoly

## Description
Creates a slab object from the referenced polyline. The current settings for the slab object are used to create the new slab.

```pascal
PROCEDURE SlabFromPoly(poly : HANDLE);
```

```python
def vs.SlabFromPoly(poly):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|poly|HANDLE|The polyline that the slab will be created from.|

## Remarks
[[User:CBM-c-|_c_]] (2017.01.27): This is one of those objects that don't respond to [LNewObj](LNewObj.md). It also doesn't return any value on [GetBBox](GetBBox.md).
```pascal
SlabFromPoly(FSActLayer);
Locus(0, 0); { do something to have a marker }
slabHandle := PrevObj(LNewObj); { can't use LNewObj directly to fetch slab }
```

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
