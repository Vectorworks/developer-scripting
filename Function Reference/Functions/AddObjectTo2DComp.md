# AddObjectTo2DComp

## Description
Adds an object to the specified 2D component group of a symbol definition or plug-in object. Use Top/Plan if you want to add the the object into the main container of the symbol definition or plug-in object.<BR>
<BR>
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
Left and Right Cut	                9<BR>
Top/Plan		               10

```pascal
FUNCTION AddObjectTo2DComp(
				objectHandle   : HANDLE;
				objToAddHandle : HANDLE;
				component      : INTEGER): BOOLEAN;
```

```python
def vs.AddObjectTo2DComp(objectHandle, objToAddHandle, component):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Symbol definition or plug-in object.|
|objToAddHandle|HANDLE|New object to be added to the 2D component group.|
|component|INTEGER|2D component|

## See Also
VS Functions:
[Set2DComponentGroup](Set2DComponentGroup.md) 
| [Get2DComponentGroup](Get2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
