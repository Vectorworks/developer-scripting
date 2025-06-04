# GetCompAltSecFill

## Description
Gets the alternate section fill of a component in an object.

```pascal
FUNCTION GetCompAltSecFill(
				obj                      : HANDLE;
				componentIndex           : INTEGER;
				VAR alternateSectionFill : LONGINT): BOOLEAN;
```

```python
def vs.GetCompAltSecFill(obj, componentIndex):
    return (BOOLEAN, alternateSectionFill)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|alternateSectionFill|LONGINT|Returns the alternate section fill of the component.|

## Remarks
[[User:CBM-c-|_c_]]: 2016.02.03:  The Alternate Section fill is used for Roof Style components whose "Section FIll Change Point" is NOT none, which only applies to Roof Styles. It nevertheless returns the current section fill index for Slab and Wall Styles. 

; Warning: passing NIL will always return the Wall Preferences' component fill! Not the Roof's Preference component alternate fill!
: Use the handle returned by the routine [[VS:GetRoofPreferences]] to parse the Roof's defaults. 
The Roof's preferences are a very buried set which can be accessed at user level only when creating a roof from a shape using the command "Create Roof" or "Roof Face". When the dialog appears, click on the "Style" pull-down menu: its first choice is "Roof Preferences". This is to my knowledge the only method to see/edit the Roof's defaults. 

Since the Roof has no tool, you can't pick attributes using the Eyedropper Tool or the Create Similar tool.

## See Also
VS Functions:
[SetCompAltSecFill](SetCompAltSecFill.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
