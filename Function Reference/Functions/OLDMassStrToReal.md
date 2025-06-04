# OLDMassStrToReal

## Description
Converts mass string to real number in grams and returns TURE on success. If no unit mark is specified, string is assumed in document units.

```pascal
FUNCTION OLDMassStrToReal(
				massString    : STRING;
				VAR realValue : REAL): BOOLEAN;
```

```python
def vs.OLDMassStrToReal(massString):
    return (BOOLEAN, realValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|massString|STRING|   |
|realValue|REAL|   |

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
