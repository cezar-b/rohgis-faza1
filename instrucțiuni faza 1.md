# __Partea I. Instrucțiuni de curățare pentru Toponime__

## 1. __Rezolvare diacritice și corectare toponime__.

1. Înlocuire `ş` cu `ș`    
2. Înlocuire `ţ` cu `ț`
3. Înlocuire `Ş` cu `Ș`
4. Înlocuire `Ţ` cu `Ț`
5. Eliminarea rîndului `Totalul comunei`, dacă există.
6. Eliminare cratime la despărțirea în silabe, dacă e cazul:  
    înlocuire `-([a-zșțăîâ])` cu `$1`  
    dar atenție la toponimele de forma _Satu-de-sus_, unde cratimele sunt corecte.

## 2. __Îmbunătățire formatare__

1. Elimină tab-uri inițiale: 
    înlocuiește `\t` cu `blanc` (_un spațiu_)
2. Elimină rîndurile cu informații suplimentare:  
    înlocuiește `^A\..*` cu nimic; se repetă și se adaptează în caz că există linii care încep cu altă literă  
    înlocuiește `^$` cu nimic

## 3. __Pregătire formatare nouă__

1. Elimină rîndurile noi:  
    înlocuiește `$` cu `blanc` (_un spațiu_)  
2. Formatare tip tabel:  
    înlocuiește `([a-zA-ZȘȚÎăîâșț-]+) (D\. K\. .*?km\.)` cu `\n$1\t$2\t`  
    _dacă comuna e reședință de plasă, în expresia de căutare se mai introduce un `\*`_
3. Tab-uri noi:  
    înlocuiește `(\(.*?\))` cu `\t$1\n\t`  
4. Tab triplu pe liniile începînd cu _nr. 2_:  
    înlocuiește `^\t` cu `\t\t\t`  
5. Steluța (semnul de reședință) pe coloană proprie:  
    înlocuiește ` (\*)` cu `$1\t`
6. Dacă satul reședință nu e primul în listă, va rămîne un tab în plus, care trebuie eliminat:  
    înlocuiește `^\t\t\t(\*)` cu `\t\t$1`
7. În comuna unde satul de la numărul 1 nu e reședința, trebuie adăugat un tab în fața lui 1:  
    înlocuiește ` 1\.` cu `\t 1.` (_atenție la spații suplimentare!_)
7. Elimină rîndurile goale:  
    înlocuiește `^\t\t\t $` cu nimic  
    înlocuiește `^\t\t\t$` cu nimic  
    înlocuiește `^$` cu nimic

## 4. __Verificare rezultat__

După curățare, documentul ar trebui să arate astfel:  

![foto](https://github.com/Cezar92/rohgis-faza1/blob/master/imag/pag_2.png)


# __Partea II. Instrucțiuni de curățare pentru Numere__

## 1. __Îmbunătățirea formatării__

1. Înlocuire `\t` cu `blanc` (_un spațiu_)  

2. Înlocuire `blanc blanc` (_două spații consecutive_) cu `blanc` (_un spațiu_)

3. Eliminare cratimă și introducerea valorii zero:  
    înlocuire `—` cu `0`

4. Verifică dacă există rînduri cu mai mult de cinci numere:  
    `[0-9]+ [0-9]+ [0-9]+ [0-9]+ [0-9]+`  
    dacă da, atunci verificați cu paginile scanate și corectați manual.

5. Verifică să nu apară litere sau alte simboluri în loc de cifre sau în plus.

5. Atenție ca nu cumva ultima linie să fie goală:  
    înlocuiește `^$` cu nimic

6. Înlocuire `blanc` (_un spațiu_) cu `\t`

7. Copiază blocul de numere lîngă lista finalizată în partea I.
