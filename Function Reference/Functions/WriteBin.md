# WriteBin

## Description
Procedure WriteBin outputs the specified data to a binary file. The variable length parameter list specifies the data to be written to the file.

Supported data types include INTEGER (2-bytes), REAL (8-bytes), LONGINT (4-bytes), CHAR (1-byte) or STRING/DYNARRAY OF CHAR (see remarks).

The bytes will be written as little-endian.

Strings will require two additional INTEGER parameters: symbol count and encoding: 
: 0 – mac
: 1 – win
: 2 – system
: 3 – UTF8
: 4 – UTF16

```pascal
PROCEDURE WriteBin(z : ANY);
```

```python
def vs.WriteBin(z):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Examples
```python
WriteBin('text', 0); { string, mac }
WriteBin(1234); { number }
```

## See Also
[ReadBin](ReadBin.md) | [Open](Open.md)

## Version
Availability: from Vectorworks 2018

## Category
* [File I@O](../Categories/File%20IO.md)
