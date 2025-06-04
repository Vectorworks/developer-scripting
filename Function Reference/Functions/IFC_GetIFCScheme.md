# IFC_GetIFCScheme

## Description
Gets the active IFC version.

```pascal
FUNCTION IFC_GetIFCScheme(VAR outScheme : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetIFCScheme():
    return (BOOLEAN, outScheme)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outScheme|INTEGER|Possible out values are <b>kIFCSupportScheme_2x2 = 2 (IFC 2x2); <b>kIFCSupportScheme_2x3 = 3 (IFC 2x3) and <b>kIFCSupportScheme_2x4 = 4 (IFC 4)|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Test;
VAR
	scheme	: INTEGER;
	ok 	: BOOLEAN;
BEGIN
	ok := IFC_GetIFCScheme(scheme);
END;

RUN(Test);
```

```python
scheme	= -1
ok	= vs.IFC_GetIFCScheme(scheme)
```

## See Also
[[VCOM:VectorWorks:IFCLib:IFCEnumerations|IFC Enumeration Types]]

## Version
Availability: from Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
