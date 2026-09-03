# VDelete

## Description
Procedure VDelete deletes the specified saved view.

```pascal
PROCEDURE VDelete(name : STRING);
```

```python
def vs.VDelete(name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of view to be deleted.|

## Examples
#### VectorScript ####
```pascal
VDelete('Detail A-A');
```
#### Python ####
```python

```

```pascal
BEGIN
	VRestore ('myTempView00000001');
	VDelete ('myTempView00000001');
END;

{restore the doc view before the plugin envocation}
VRestore('UpdateObjectsTempView');
VDelete('UpdateObjectsTempView');

		SetRField(objHand, kSeatingObjectName, 'RowSpacing', Num2Str(8, RowSpacing));
		gRowSpacing := RowSpacing;
		END;
	VRestore ('__SeatingLayoutTempView');
	VDelete ('__SeatingLayoutTempView');
END;
```
```python
vs.VDelete('Example')
```

## Version
Availability: from All Versions

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
