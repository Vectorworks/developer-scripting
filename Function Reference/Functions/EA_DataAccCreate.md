# EA_DataAccCreate

## Description
Returns accessory index. The function opens a 'session' to energy analysis plugin for particular handle. The handle is a handle to record format or to object.

```pascal
FUNCTION EA_DataAccCreate(
				type : INTEGER;
				h    : HANDLE): INTEGER;
```

```python
def vs.EA_DataAccCreate(type, h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|type|INTEGER|   |
|h|HANDLE|   |

## Examples
==== VectorScript ====
```pascal
{ _c_ 2022.04.14:
example procedure for changing lambda values of a wall style
Thanks to Kostadin Ivanov for his precious hint: 
We can't change only 1 component! We must  delete them all, then load a complete set.

Python only: EA_DataAccCompGet can't be used for VW before 2022 SP4, the index returned is gibberish. 
}

PROCEDURE TestEnergos;
TYPE
    ENERGS = STRUCTURE
        idx        : INTEGER; { index }
        inc        : BOOLEAN; { include }
        lbd        : REAL; { lambda }
        thk        : REAL; { thickness }
    END;
VAR
    eData : DYNARRAY[] OF ENERGS;
    str : DYNARRAY[] OF CHAR;
    style : HANDLE;
    i, numComps, comp2override, acc : INTEGER;
    lbda : REAL;

BEGIN
    style := GetObject('Wall Style'); { make sure you have in the document a wall style named "Wall Style" }
    str := 'Exited without doing nothing'; { init dynarray of chars }
    
    IF (style <> NIL) & GetNumberOfComponents(style, numComps) & (numComps > 0) THEN BEGIN
        comp2override := IntDialog(Concat('Choose a an index from 1 to ', numComps), '1');

        IF NOT DidCancel THEN BEGIN
            str := 'Component data:';
            acc := EA_DataAccCreate(300, style);  { open energos session for the accessor }
            { 300 = Walls, 400 = Slabs, 500 = Roofs }
           {  more infos [https://developer.vectorworks.net/index.php/VS:Energos_Thirdparty_Support }
            
            { access to comp index is 0-based }
            comp2override := comp2override -1;
            numComps := numComps -1;
            ALLOCATE eData[0..numComps];
            
            FOR i := 0 TO numComps DO BEGIN
                eData[i].idx := i; { need to init: in VW before 2022 SP4 it is a VAR }
                EA_DataAccCompGet(acc, eData[i].idx, eData[i].inc, eData[i].lbd, eData[i].thk);
            END;            
            
            lbda := RealDialog(Concat('Enter a new value for the lambda of component ', comp2override +1), Concat(eData[comp2override].lbd)); 
            IF NOT DidCancel THEN BEGIN
                EA_DataAccCompDel(acc); { deletes all components }
                eData[comp2override].lbd := lbda; { index 0-based, overwrites lambda of chosen component }
            
                { restore components, load them as string for an info dialog at the end }
                FOR i := 0 TO numComps DO BEGIN
                    EA_DataAccCompAdd(acc, eData[i].inc, eData[i].lbd, eData[i].thk);
                    str := Concat(str, Chr(13), eData[i].idx, ': lambda ', eData[i].lbd)
                END;
                    
                EA_DataAccCpyInto(acc, style); { copy values into the style }
                EA_DataAccSave(acc); { save }
            END;
            
            EA_DataAccDelete(acc); { close energos session for the accessor }
        END;
    END;
    
    AlrtDialog(str); { info dialog }
END;
RUN( TestEnergos );
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
