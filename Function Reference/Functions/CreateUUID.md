# CreateUUID

## Description
Creates a string representing universe unique identifier. The string is in the form: '{00000000-0000-0000-0000-000000000000}'

```pascal
FUNCTION CreateUUID : STRING;
```

```python
def vs.CreateUUID():
    return STRING
```

## Examples
```pascal
resultStr := CreateUUID;
```
```python
import vs

# Creates a string representing universe unique identifier.
text = vs.CreateUUID()
vs.Message('CreateUUID returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
