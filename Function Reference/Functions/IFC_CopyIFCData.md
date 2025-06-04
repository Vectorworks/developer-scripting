# IFC_CopyIFCData

## Description
Copies IFC data from one object to another

```pascal
FUNCTION IFC_CopyIFCData(
				hSource      : HANDLE;
				hDestination : HANDLE;
				inMode       : INTEGER): BOOLEAN;
```

```python
def vs.IFC_CopyIFCData(hSource, hDestination, inMode):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSource|HANDLE|Handle source to object.|
|hDestination|HANDLE|Handle to destination object.|
|inMode|INTEGER|Options for copying. Possible values are 0 (copy always, new UUID); 1 (copy always, keep the old UUID); 2(copy, if same type, new UUID) and 3(copy, if same type, keep the old UUID).|

## Examples
Assume we want to copy IFC data from a Space object to a Table object.

#### VectorScript ####
```pascal
PROCEDURE CopyIFCData;
VAR
	hSource 	: HANDLE;
	hDestination 	: HANDLE;
	ok 		: BOOLEAN;
BEGIN
	hSource         := GetObject('Dining Room'); {Space Object}
	hDestination    := GetObject('Dining Table'); {Table Object}
	ok              := IFC_CopyIFCData(hSource, hDestination, 0); {ok returns TRUE, IFC data copied, new UUID created}
	ok              := IFC_CopyIFCData(hSource, hDestination, 1); {ok returns TRUE, IFC data copied, old UUID kept}
	ok              := IFC_CopyIFCData(hSource, hDestination, 2); {ok returns FALSE, IFC data not copied, different entity types}
	ok              := IFC_CopyIFCData(hSource, hDestination, 3); {ok returns FALSE, IFC data not copied, different entity types}
END;

RUN(CopyIFCData);
```
#### Python ####
```python
hSource = vs.GetObject("Dining Room"); #Space Object
hDestination = vs.GetObject("Dining Table"); #Table Object
ok = vs.IFC_CopyIFCData(hSource, hDestination, 0); #ok returns TRUE, IFC data copied, new UUID created
ok = vs.IFC_CopyIFCData(hSource, hDestination, 1); #ok returns TRUE, IFC data copied, old UUID kept
ok = vs.IFC_CopyIFCData(hSource, hDestination, 2); #ok returns FALSE, IFC data not copied, different entity types
ok = vs.IFC_CopyIFCData(hSource, hDestination, 3); #ok returns FALSE, IFC data not copied, different entity types
```

## Version
Available from: Vectorworks 2011.

## Category
* [IFC](../Categories/IFC.md)
