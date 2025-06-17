# Trunc

## Description
Truncates the decimal portion of the specified REAL number, returning the result as a LONGINT value.

Note that direct assignment of a REAL to a LONGINT will result in rounding the REAL to the ''nearest'' LONGINT, whereas Trunc always ''rounds down'' (if the number is positive).

```pascal
FUNCTION Trunc(v : REAL): LONGINT;
```

```python
def vs.Trunc(v):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Real value to truncate.|

## Remarks
[[User:CBM-c-|_c_]], 2015.05.23: Pay attention when using Trunc with very large numbers exceeding the Longint limit: [http://en.wikipedia.org/wiki/2147483647 2147483647]].

```pascal
num :=  1000000000000.23456789; { a very large number }
AlrtDialog(Concat(num)); { --> 1000000000000.23 loss of digits }
AlrtDialog(Concat('prec 2: ', Num2Str(2, num) )); { --> 1000000000000.23  OK }
AlrtDialog(Concat('prec -1: ', Num2Str(-1, num) )); { --> 1,0000000000e+12  OK }
AlrtDialog(Concat('prec -2: ', Num2Str(-2, num) )); { --> 1,00000000000235e+12  OK }
AlrtDialog(Concat('prec -3: ', Num2Str(-3, num) )); { --> empty! }
AlrtDialog(Concat('prec -4: ', Num2Str(-4, num) )); { --> empty! }

AlrtDialog(Concat('Trunc: ', Trunc(num) )); { --> 2147483647 fully wrong }
));
 ```

## Examples
#### VectorScript ####
```pascal
Trunc(235.04); { returns 235 }
Trunc(235.94); { returns 235 }
Trunc(0.94); { returns 0 }
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
