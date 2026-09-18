# ClassNum

## Description
Returns the total number of classes in the active document.

```pascal
FUNCTION ClassNum : LONGINT;
```

```python
def vs.ClassNum():
    return LONGINT
```

## Examples
#### VectorScript ####
```pascal
numOfClasses:= ClassNum;
```
#### Python ####
```python
numOfClasses = vs.ClassNum()
```

```pascal
resultN := ClassNum;
```
```python
import vs

# Returns the total number of classes in the active document.
count = vs.ClassNum()
vs.Message('ClassNum returned: ' + str(count))
```

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
