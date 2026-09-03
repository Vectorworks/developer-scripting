# DelName

## Description
Procedure DelName deletes an object name from a VectorWorks document. The associated object is not affected by the name deletion.

```pascal
PROCEDURE DelName(name : STRING);
```

```python
def vs.DelName(name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Object name to be deleted.|

## Examples
```pascal
DelName('Example');
```
```python
import vs

# Procedure DelName deletes an object name from a VectorWorks document.
name = 'Example'

vs.DelName(name)
```

## Version
Availability: from All Versions

## Category
* [Object Names](../Categories/Object%20Names.md)
