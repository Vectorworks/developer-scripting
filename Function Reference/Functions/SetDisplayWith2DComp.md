# SetDisplayWith2DComp

## Description
Sets whether a 3D object in a symbol definition or plug-in object is shown when the specified 2D component is shown.<BR>
                                                                                                                       Table - 2D components<BR>
2D component		Constant<BR>
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
FUNCTION SetDisplayWith2DComp(
				objectHandle : HANDLE;
				component    : INTEGER;
				isVisible    : BOOLEAN): BOOLEAN;
```

```python
def vs.SetDisplayWith2DComp(objectHandle, component, isVisible):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|3D object handle.|
|component|INTEGER|2D component.|
|isVisible|BOOLEAN|Visibility of the object when the 2D component is shown.|

## See Also
VS Functions:
[Set2DComponentGroup](Set2DComponentGroup.md) 
| [Get2DComponentGroup](Get2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
