# Partea I. Instrucțiuni de curățare pentru Toponime

## 1. __Rezolvare diacritice și corectare toponime__.

1. Înlocuire `ş` cu `ș`    
2. 1b. Înlocuire 
3. 1c. Eliminare cratime la despărțirea în silabe, dacă e cazul:
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
4. Tab dublu pe liniile începînd cu _nr. 2_:  
        înlocuiește `^\t` cu `\t\t\t`  
5. Steluța (semnul de reședință) pe coloană proprie:  
        înlocuiește ` (\*)` cu `$1\t`