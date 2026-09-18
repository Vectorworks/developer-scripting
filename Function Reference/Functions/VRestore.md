# VRestore

## Description
Procedure VRestore restores the specified saved view (i.e., sheet name).

```pascal
PROCEDURE VRestore(name : STRING);
```

```python
def vs.VRestore(name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of view to be displayed.|

## Examples
```pascal
BEGIN
	VRestore ('myTempView00000001');
	VDelete ('myTempView00000001');
END;

{restore the doc view before the plugin envocation}
VRestore('UpdateObjectsTempView');
VDelete('UpdateObjectsTempView');

		BEGIN
		SetRField(objHand, kSeatingObjectName, 'RowSpacing', Num2Str(8, RowSpacing));
		gRowSpacing := RowSpacing;
		END;
	VRestore ('__SeatingLayoutTempView');
	VDelete ('__SeatingLayoutTempView');
END;
```
```python
import vs

# , sheet name).
name = 'Example'

vs.VRestore(name)
```

## Version
Availability: from All Versions

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
