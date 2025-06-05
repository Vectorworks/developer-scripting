# GetFldType

## Description
Returns a constant indicating the data type of a specified field in the referenced record.

Please refer to the [Script Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#record---worksheet-field-types) for specific field data types and formatting.


For Plug-in Object Parameter Records, the field types are documented in the [Scirpt Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#plug-in-object-parameter-record-field-types).

```pascal
FUNCTION GetFldType(
				h : HANDLE;
				t : INTEGER): INTEGER;
```

```python
def vs.GetFldType(h, t):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to record.|
|t|INTEGER|Field index (range of 1 - n).|

## Remarks
Returns a constant indicating which type of field is specified by the field number &quot;t&quot; of record &quot;h&quot;.  The field type constants are listed in an appendix in the vectorscript manual.

In the appendix, the field types for worksheets and data records are listed, but the field types for parameter records (e.g., plug-in object records) are different...

Data Records:

| Constant | Description                |
|----------|---------------------------|
| 1        | Integer                   |
| 2        | Boolean                   |
| 3        | Number-general            |
| 4        | Text                      |
| 5        | Number-decimal            |
| 6        | Number-decimal w/ commas  |
| 7        | Number-scientific         |
| 8        | Number-fractional         |
| 9        | Number-dimension          |
| 10       | Number-angle              |
| 11       | Number-date/time          |

PIO Records:

| Constant | Description         |
|----------|--------------------|
| 1        | Integer            |
| 2        | Boolean            |
| 3        | Number             |
| 4        | Text               |
| 7        | Dimension          |
| 8        | Pop-Up             |
| 9        | Radio Buttons      |
| 10       | Control Point X    |
| 11       | Control Point Y    |
| 14       | Static Text Label  |
| 18       | Classes Pop-up     |
| 19       | Layer Pop-up       |
| 20       | Angle              |
| 21       | Area               |
| 22       | Volume             |
| 23       | Class              |
| 24       | Material           |
| 25       | Fill               |
| 26       | Pen Style          |
| 27       | Pen Weight         |
| 28       | Color              |
| 29       | Texture            |
| 30       | Symbol Definition  |

## Examples
#### VectorScript ####
```pascal
fieldType:=GetFldType(recordHandle,3);
```
#### Python ####
```python
fieldType = vs.GetFldType(recordHandle,3)
```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
