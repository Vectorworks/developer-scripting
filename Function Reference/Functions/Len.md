# Len

## Description
Function Len returns the length of the specified string value.

```pascal
FUNCTION Len(v : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.Len(v):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|DYNARRAY[] of CHAR|Source string.|

## Remarks
<b>Vectorworks 2018</b>: This function will behave differently when used during dialog creation. 
:When used between [[VS:CreateLayout]], [[VS:CreateResizableLayout]] and [[VS:RunLayoutDialog]] and [[VS:RunLayoutDialogN]] it will return the length of a string in bytes count, mimicking dialog units.
:This means that the number might not be what you expect during the creation of the layout. In this case where this is a problem, you can use it outside the creation and move the value via a variable.
:This was needed to solve alignment issues with Japanese and Unicode in Vectorworks 2018.

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
