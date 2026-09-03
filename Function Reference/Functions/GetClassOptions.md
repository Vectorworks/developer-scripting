# GetClassOptions

## Description
Returns the class visibility setting for the active document.

```pascal
FUNCTION GetClassOptions : INTEGER;
```

```python
def vs.GetClassOptions():
    return INTEGER
```

## Examples
```pascal
resultN := GetClassOptions;
```
```python
curClassVis = vs.GetClassOptions()
vs.SetClassOptions( 5 ) #Set to Show/Snap/Modify to fix VB-116777
```

## See Also
VS Functions:
[SetClassOptions](SetClassOptions.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Classes](../Categories/Classes.md)
