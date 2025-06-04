# WriteLnMac

## Description
Writes a line of data to a text file using Macintosh character encoding for extended ASCII characters (128-255). This allows extended character data to be properly read and displayed by VectorWorks on Windows systems (VectorWorks by default uses Macintosh encoding for extended character values).

The line of data written to file is terminated with a return character combination appropriate for the platform on which the file is being written.

```pascal
PROCEDURE WriteLnMac(z : ANY);
```

```python
def vs.WriteLnMac(z):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
CONST
Vendor = 'ACME';
Price = 123.45;
Tax = 1.07;
BEGIN
Open('Output.txt');
WriteLnMac('Mfr/Cost: ', Vendor, '/', Price + Tax);
Close('Output.txt');
END;
RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[WriteLn](WriteLn.md)

## Version
Availability: from VectorWorks9.0

## Category
* [File I@O](../Categories/File%20IO.md)
