# NameClass

## Description
Creates a new class in a VectorWorks document, which then become the active class.
If the specified class already exists, then it will become the active class of the document.

Note: Class names cannot exceed 63 characters.

```pascal
PROCEDURE NameClass(className : STRING);
```

```python
def vs.NameClass(className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Examples
#### VectorScript ####
```pascal
NameClass('Revisions');
Rect(4,4,6,6);

{Create a class 'Revisions' in the document}
{The rectangle is then assigned this class }
```
#### Python ####
```python

```

```pascal
BEGIN
	IF IsTextureableObject(hobj) THEN BEGIN
		IF Name2Index(ClassName) = 0 THEN BEGIN
			activeClName:= ActiveClass;
			NameClass(ClassName);
			NameClass(activeClName);
		END;

BEGIN	{ Main }
	{DselectAll;}
	{IF SetUpObject( gPluginName, gPluginH, recordH, wallH, saveClass, noneClass ) THEN}
	{BEGIN}
		IF kUseContainerClass THEN NameClass( GetClass( gPluginH ) );

BEGIN
CurrentClass:= ActiveClass;
NameClass(PartClass);
NameClass(CurrentClass);
END;
```
```python
if objType == 94:
	vs.NameClass( className )

if vs.GetTypeN(h) == 94:
	vs.NameClass(className)
```
See also in tutorials: [01. Draw a Room with Walls](ai%20examples/01_DrawRoomWithWalls.md), [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md), [20. Read a Polyline and Build Walls Along Its Path](ai%20examples/20_PolylineToWalls.md)

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
