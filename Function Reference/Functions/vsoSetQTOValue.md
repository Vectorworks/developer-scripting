# vsoSetQTOValue

## Description
Set a requested QTO value during event 84 (kParametricGetQTOValue). Check the requested QTO value by using vsoGetQTOFunction. 'valueType' [0:real; 1:integer; 2:string] determines which parameter is considered for the value, the others can be empty (zero).

```pascal
PROCEDURE vsoSetQTOValue(
				valueType : INTEGER;
				int       : INTEGER;
				real      : REAL;
				string    : DYNARRAY[] of CHAR);
```

```python
def vs.vsoSetQTOValue(valueType, int, real, string):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|valueType|INTEGER|   |
|int|INTEGER|   |
|real|REAL|   |
|string|DYNARRAY[] of CHAR|   |

## Examples
```pascal
vsoSetQTOValue(1, 2, 1.0, string);
```
```python
import vs

# Set a requested QTO value during event 84 (kParametricGetQTOValue).
valueType = 0
int = 1
real = 1.0
string = 'Example'

vs.vsoSetQTOValue(valueType, int, real, string)
```

## Version
Availability: from Vectorworks 2022

## Category
* [Object Events](../Categories/Object%20Events.md)
