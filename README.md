# __Partea I. Instrucțiuni de curățare pentru Toponime__

## 1. __Rezolvare diacritice și corectare toponime__.

1. Înlocuire `ş` cu `ș`    
2. Înlocuire ...
3. Eliminare cratime la despărțirea în silabe, dacă e cazul:  
    înlocuire `-([a-zșțăîâ])` cu `$1`

## 2. __Îmbunătățire formatare__

1. Elimină tab-uri inițiale: 
    înlocuiește `\t` cu `blanc` (_un spațiu_)
2. Eliminăm rîndurile cu informații suplimentare:
    înlocuiește `^A\..*` cu nimic; se repetă și se adaptează în caz că există linii care încep cu altă literă
    înlocuiește `^$` cu nimic

## 3. __Pregătire formatare nouă__

1. Eliminăm rîndurile noi:  
    înlocuiește `$` cu `blanc` (_un spațiu_)  
2. Formatare tip tabel:  
    înlocuiește `([a-zA-ZȘȚÎăîâșț-]+) (D\. K\. .*?km\.)` cu `\n$1\t$2\t`  
3. Tab-uri noi:  
    înlocuiește `(\(.*?\))` cu `\t$1\n\t`  
4. Tab triplu pe liniile începînd cu _nr. 2_:  
    înlocuiește `^\t` cu `\t\t\t`  
5. Steluța (semnul de reședință) pe coloană proprie:  
    înlocuiește ` (\*)` cu `$1\t`
6. Dacă satul reședință nu e primul în listă, va rămîne un tab în plus, care trebuie eliminat:  
    înlocuiește `^\t\t\t(\*)` cu `\t\t$1`
7. În comuna unde satul de la numărul 1 nu e reședința, trebuie adăugat un tab în fața lui 1:  
    înlocuiește ` 1\.` cu `\t 1.`
7. Eliminăm rîndurile goale:  
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

## 2. __Executarea script-ului__

1. Se pregătesc fișierele conform situației stabilite.
2. Se rulează script-ul.

## 3. __Pregătire date__

1. Înlocuire `,` cu `\n`  

2. Înlocuire `blanc` (_un spațiu_) cu `\t`
