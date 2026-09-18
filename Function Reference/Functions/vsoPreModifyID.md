# vsoPreModifyID

## Description
Sends the event to a Script object before modifying.

```pascal
FUNCTION vsoPreModifyID(message : LONGINT) : INTEGER;
```

```python

def vs.vsoPreModifyID(message):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT||

## Examples
```pascal
resultN := vsoPreModifyID(1);
```
```python
import vs

# Sends the event to a Script object before modifying.
message = 'Hello Vectorworks'

resultN = vs.vsoPreModifyID(message)
vs.Message('vsoPreModifyID returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2024

## Category
* [Object Events](../Categories/Object Events.md)
