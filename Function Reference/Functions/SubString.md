# SubString

## Description
Function SubString splits the Text string using characters specified in the var "Delimiter" and returns the token located at the Index position. <BR>
The first token is located at index 1. <BR>
If there is an error the function returns ''(empty string).<BR>
If index is less than 1 or greater than max number of tokens the function returns ''(empty string).

```pascal
FUNCTION SubString(
				text      : DYNARRAY[] of CHAR;
				delimiter : STRING;
				index     : INTEGER): DYNARRAY[] of CHAR;
```

```python
def vs.SubString(text, delimiter, index):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|text|DYNARRAY[] of CHAR|   |
|delimiter|STRING|   |
|index|INTEGER|   |

## Examples
```python
middleStr := SubString('Left;Middle;Right', ';', 2);
```

## Version
Availability: from Vectorworks 2014

## Category
* [Strings](../Categories/Strings.md)
