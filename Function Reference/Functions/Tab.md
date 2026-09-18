# Tab

## Description
Procedure Tab writes a tab character to the current output file.

```pascal
PROCEDURE Tab(n : INTEGER);
```

```python
def vs.Tab(n):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|n|INTEGER|Number of tab characters to be written to file.|

## Examples
#### VectorScript ####
```pascal
Tab(2);
{writes two tabs to the output file}
```
#### Python ####
```python

```

```pascal
BEGIN
	IF numNestedFolders > 1 THEN
		Tab (numNestedFolders - 1);

BEGIN
Tab(1);
Writeln ('Merged Item  :  Old ',ExistLayer[RefItem,1],'New ',NewLayer[I,1],' Num of Elements ',NumSObj(ActLayer));
END;

BEGIN
	Write(exportStr);
	TAB(1);
END {IF TabExport}
ELSE {Export CSV}
BEGIN
	Write(exportStr,',');
```
```python
vs.Tab(n)
```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
