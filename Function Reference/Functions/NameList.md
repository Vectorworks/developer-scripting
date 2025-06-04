# NameList

## Description
Function NameList returns the specified object name from the object name list.

```pascal
FUNCTION NameList(index : LONGINT): STRING;
```

```python
def vs.NameList(index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|LONGINT|Name list position index (in a arange of 1 - n).|

## Remarks
([[User:Orso.b.schmid| Orso]], 2008.03.22): It looks like the name list only increases. If you remove from a document some named items, their position at index in the list will not be overwritten, an empty space will be left. New items always add an item to the end of the nameList. So, DO assign a LONGINT to that "index" variable. On old files where you have been working a lot, it is not seldom to observe a nameList of 10000 items of more, most of them empty. Just mind this, in case you are looping down.

Since you'll most likely have loads of empty strings looping down the nameList indexes, it is advisable to compare the length of the string instead of the emptiness of the string. A string comparison in VS is infinitely slower than a numerical check (length of the string)
<code lang="pas">Len(NameList(index)) > 0 { very fast }
NameList(index) <> '' { very slow }</code>

Names in both NameList and LayerList are subject to the following rules:
* names are case insensitive: "bla" = "BLA"
* diacriticals are ignored and reduced to their carrying character below ASCII 128: "blä" = 'bla":

Layer names don't belong to the NameList. You can have a class and a layer both named "xxx" and no name collision will arise. There is thus a fundamental difference in behavior between NameList and [[VS:GetObject| GetObject]]. Pay attention:
<code lang="pas">
GetObject('xxx') { an obj called "xxx" is present and is not a layer > returns the obj }
GetObject('xxx') { only a layer called "xxx" is present > returns the layer }
GetObject('xxx') { both an obj and a layer called "xxx" are present > returns the obj }
</code>

NameList(index) would never return the layer. With [[VS:GetObject| GetObject]] you can fetch the layer, but you'll get preferably the item belonging to the NameList if both present, in this case the obj "xxx', but not the layer 'xxx'.
If no item in the NameList carries the name searched with [[VS:GetObject| GetObject]], then the LayerList will be taken into account.

## Version
Availability: from All Versions

## Category
* [Object Names](../Categories/Object%20Names.md)
