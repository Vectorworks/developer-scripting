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

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
