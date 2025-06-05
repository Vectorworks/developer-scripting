# SymbolToGroup

## Description
Converts referenced symbol to group using the specified conversion options.

**Table - Convert Actions**

| Convert Action                     | Constant |
|-------------------------------------|----------|
| Don't convert subobjects            | 0        |
| Convert plug-in and symbol subobjects| 1       |
| Convert all subobjects              | 2        |

```pascal
PROCEDURE SymbolToGroup(
				h             : HANDLE;
				convertAction : INTEGER);
```

```python
def vs.SymbolToGroup(h, convertAction):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the symbol|
|convertAction|INTEGER|Conversion action:|0 - don't convert subobjects|1 - convert subobjects that are plug-ins and symbols|2 - convert all subobjects|

## Remarks
([[User:CBM-c-|_c_]], 2014.09.14): Upon success, this creates a group which doesn't respond to ''LNewObj''. It actually disables ''LNewObj'', which will return NIL, unregarded what you created before running ''SymbolToGroup''

The handle to the group can be fetched storing a handle to the object BEFORE the symbol on drawing, then fetching the next object:
<code lang="pas">
PROCEDURE Test;
VAR
	h : HANDLE;
BEGIN
	h := PrevObj(FSActLayer); { store "h" as placeholder }

	{ FSActLayer must be a symbol on drawing }
	IF (FSActLayer <> NIL) & (GetType(h) = 15) THEN BEGIN
		SymbolToGroup(FSActLayer, 2);
		
		{ fetch group starting from placeholder "h" }
		Message(GetType(NextObj(h))); { <-- NextObj(h) should return 11: is the new group }
	END ELSE
		AlrtDialog('Select a symbol on drawing!');
END;
RUN(Test);</code>

## Version
Availability: from VectorWorks 10.0

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
