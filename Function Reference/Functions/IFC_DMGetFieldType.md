# IFC_DMGetFieldType

## Description
Gets indicated field type from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetFieldType(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING;
				VAR outType    : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetFieldType(inStrObjName, inStrEntryName, inStrFieldName):
    return (BOOLEAN, outType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|outType|INTEGER|   |

## Remarks
*\_c\_* (2020.06.11) From the SDK:

**Table - Field Types**

| Value                  | Integer value | Description |
|------------------------|---------------|-------------|
| UNKNOWN                | 0             |             |
| IDENTIFIER             | 1             |             |
| DOUBLE                 | 2             |             |
| BOOLEAN                | 3             |             |
| INTEGER                | 4             |             |
| NUMBER                 | 5             |             |
| LOGICAL                | 6             |             |
| STRING                 | 7             |             |
| ENUMERATION            | 8             |             |
| SELECT                 | 9             |             |
| ARRAY_IDENTIFIER       | 10            |             |
| ARRAY_DOUBLE           | 11            |             |
| ARRAY_BOOLEAN          | 12            |             |
| ARRAY_INTEGER          | 13            |             |
| ARRAY_NUMBER           | 14            |             |
| ARRAY_LOGICAL          | 15            |             |
| ARRAY_STRING           | 16            |             |
| ARRAY_ENUMERATION      | 17            |             |
| ARRAY_SELECT           | 18            |             |
| LIST_IDENTIFIER        | 19            |             |
| LIST_DOUBLE            | 20            |             |
| LIST_BOOLEAN           | 21            |             |
| LIST_INTEGER           | 22            |             |
| LIST_NUMBER            | 23            |             |
| LIST_LOGICAL           | 24            |             |
| LIST_STRING            | 25            |             |
| LIST_ENUMERATION       | 26            |             |
| LIST_SELECT            | 27            |             |
| SET_IDENTIFIER         | 28            |             |
| SET_DOUBLE             | 29            |             |
| SET_BOOLEAN            | 30            |             |
| SET_INTEGER            | 31            |             |
| SET_NUMBER             | 32            |             |
| SET_LOGICAL            | 33            |             |
| SET_STRING             | 34            |             |
| SET_ENUMERATION        | 35            |             |
| SET_SELECT             | 36            |             |
| BINARY                 | 37            |             |
| LIST_BINARY            | 38            |             |
| LIST_LIST_IDENTIFIER   | 39            |             |
| LIST_LIST_DOUBLE       | 40            |             |
| LIST_LIST_BOOLEAN      | 41            |             |
| LIST_LIST_INTEGER      | 42            |             |
| LIST_LIST_NUMBER       | 43            |             |
| LIST_LIST_LOGICAL      | 44            |             |
| LIST_LIST_STRING       | 45            |             |
| LIST_LIST_ENUMERATION  | 46            |             |
| LIST_LIST_SELECT       | 47            |             |

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
