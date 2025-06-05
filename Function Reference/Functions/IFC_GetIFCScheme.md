# IFC_GetIFCScheme

## Description
Gets the active IFC version.

```pascal
FUNCTION IFC_GetIFCScheme(VAR outScheme : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetIFCScheme():
    return (BOOLEAN, outScheme)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outScheme|INTEGER|Possible out values are <b>kIFCSupportScheme_2x2 = 2 (IFC 2x2); <b>kIFCSupportScheme_2x3 = 3 (IFC 2x3) and <b>kIFCSupportScheme_2x4 = 4 (IFC 4)|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
	scheme	: INTEGER;
	ok 	: BOOLEAN;
BEGIN
	ok := IFC_GetIFCScheme(scheme);
END;

RUN(Test);
```

```python
scheme	= -1
ok	= vs.IFC_GetIFCScheme(scheme)
```

## Remarks
### EIFCSupportSchema
[buildingSMART’s](https://www.buildingsmart.org/about/what-is-openbim/ifc-introduction) technical core is based around a common data schema (model) called IFC that makes it possible to hold and exchange relevant data between different software applications. That enumeration represents different versions of the IFC model (IFC schema).

| Value                   | Integer value | Description |
|-------------------------|---------------|-------------|
| kIFCSupportScheme_2x2   | 0             | IFC 2x2     |
| kIFCSupportScheme_2x3   | 1             | IFC 2x3     |
| kIFCSupportScheme_2x4   | 2             | IFC 4       |

### ESourceValueType
This enumeration is used as out parameter in functions [IFC_GetEntityProp2](IFC_GetEntityProp2.md) and [IFC_GetPsetProp2](IFC_GetPsetProp2.md) called **outMap**.

| Value         | Integer value | Description                                                        |
|---------------|---------------|--------------------------------------------------------------------|
| eNotSet       | -1            | The source of the value is unknown. It could be treated as error code. |
| eFromInstance | 0             | The value comes from instance.                                     |
| eFromMapping  | 1             | The value comes from Data mapping.                                 |

### ERecordIFCType
This enumerations is used by VWFC classes to recognize the type of IFC records. For common purposes use **None** value. Use the other values only if you are sure for the type. The difference betwen types is in the record structure.

| Value | Integer value | Description                                                                 |
|-------|---------------|-----------------------------------------------------------------------------|
| None  | 0             | Default values, it is used to identify the type of record by the IFC library.|
| IFC   | 1             | IFC Entity                                                                  |
| PSet  | 2             | Pset                                                                        |
| IFCTag| 3             | IFC Tag                                                                     |

### EIfcType
This enumeration is of type Sint32 and represents the IFC type of fields.

| Value                        | Integer value |
|------------------------------|--------------|
| kIfcType_UNKNOWN             | 0            |
| kIfcType_IDENTIFIER          | 1            |
| kIfcType_DOUBLE              | 2            |
| kIfcType_BOOLEAN             | 3            |
| kIfcType_INTEGER             | 4            |
| kIfcType_NUMBER              | 5            |
| kIfcType_LOGICAL             | 6            |
| kIfcType_STRING              | 7            |
| kIfcType_ENUMERATION         | 8            |
| kIfcType_SELECT              | 9            |
| kIfcType_ARRAY_IDENTIFIER    | 10           |
| kIfcType_ARRAY_DOUBLE        | 11           |
| kIfcType_ARRAY_BOOLEAN       | 12           |
| kIfcType_ARRAY_INTEGER       | 13           |
| kIfcType_ARRAY_NUMBER        | 14           |
| kIfcType_ARRAY_LOGICAL       | 15           |
| kIfcType_ARRAY_STRING        | 16           |
| kIfcType_ARRAY_ENUMERATION   | 17           |
| kIfcType_ARRAY_SELECT        | 18           |
| kIfcType_LIST_IDENTIFIER     | 19           |
| kIfcType_LIST_DOUBLE         | 20           |
| kIfcType_LIST_BOOLEAN        | 21           |
| kIfcType_LIST_INTEGER        | 22           |
| kIfcType_LIST_NUMBER         | 23           |
| kIfcType_LIST_LOGICAL        | 24           |
| kIfcType_LIST_STRING         | 25           |
| kIfcType_LIST_ENUMERATION    | 26           |
| kIfcType_LIST_SELECT         | 27           |
| kIfcType_SET_IDENTIFIER      | 28           |
| kIfcType_SET_DOUBLE          | 29           |
| kIfcType_SET_BOOLEAN         | 30           |
| kIfcType_SET_INTEGER         | 31           |
| kIfcType_SET_NUMBER          | 32           |
| kIfcType_SET_LOGICAL         | 33           |
| kIfcType_SET_STRING          | 34           |
| kIfcType_SET_ENUMERATION     | 35           |
| kIfcType_SET_SELECT          | 36           |
| kIfcType_BINARY              | 37           |
| kIfcType_LIST_BINARY         | 38           |
| kIfcType_LIST_LIST_IDENTIFIER| 39           |
| kIfcType_LIST_LIST_DOUBLE    | 40           |
| kIfcType_LIST_LIST_BOOLEAN   | 41           |
| kIfcType_LIST_LIST_INTEGER   | 42           |
| kIfcType_LIST_LIST_NUMBER    | 43           |
| kIfcType_LIST_LIST_LOGICAL   | 44           |
| kIfcType_LIST_LIST_STRING    | 45           |
| kIfcType_LIST_LIST_ENUMERATION| 46          |
| kIfcType_LIST_LIST_SELECT    | 47           |

## Version
Availability: from Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
