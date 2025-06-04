# GetDisplayWith2DComp

## Description
Gets whether a 3D object in a symbol definition or plug-in object is shown when the specified 2D component is shown.<BR>
<BR>
                    Table - 2D components<BR>
2D component			Constant<BR>
Not Set			0<BR>
Top			1<BR>
Bottom			2<BR>
Top and Bottom Cut	                3<BR>
Front			4<BR>
Back			5<BR>
Front and Back Cut	                6<BR>
Left			7<BR>
Right			8<BR>
Left and Right Cut	                9   <BR>

```pascal
FUNCTION GetDisplayWith2DComp(
				objectHandle : HANDLE;
				component    : INTEGER): BOOLEAN;
```

```python
def vs.GetDisplayWith2DComp(objectHandle, component):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|3D object handle.|
|component|INTEGER|2D component.|

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
