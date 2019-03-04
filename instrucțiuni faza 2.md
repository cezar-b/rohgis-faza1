# __FAZA 2__

## __Partea I. Instrucțiuni de curățare pentru Toponime__

### 1. __Rezolvare diacritice și corectare toponime__.

1. Corectare toponime conform cu anexa Legii.
2. Înlocuire `ş` cu `ș`    
3. Înlocuire `ţ` cu `ț`
4. Înlocuire `Ş` cu `Ș`
5. Înlocuire `Ţ` cu `Ț`

### 2. __Îmbunătățire formatare sate__

1. **se copiază textul din Writer în Calc ca _text neformatat_.**   
2. **se șterge coloana cu cătune**  
3. **se lipește la loc în Writer ca text neformatat**  
4. ștergem numerele comunelor: înlocuire `^[0-9]+.*?\t` cu nimic.
5. înlocuire `([2-9]+)` cu `\n\t$1`; se va adapta pentru comunele care au mai mult de nouă sate.
6. șterge spațiul de la final de rînd: înlocuiește ` $` cu nimic.
7. înlocuire `\*$` cu `\t reședință`
8. **se copiază textul din Writer în Calc ca _text neformatat_**.  
9. se adaugă în Calc o nouă coloană numită `statut`, unde se completează cuvîntul `sat` pentru fiecare rînd.

### 3. __Îmbunătățire formatare cătune__

1. **se copiază textul din Writer în Calc ca _text neformatat_.**   
2. **se șterge coloana cu sate**  
3. **se lipește la loc în Writer ca text neformatat**  
4. ștergem numerele comunelor: înlocuire `^[0-9]+.*?\t` cu nimic.
5. înlocuire `([2-9]+)` cu `\n\t$1`
6. șterge spațiul de la final de rînd: înlocuiește ` $` cu nimic.
7. înlocuire `\*$` cu `\t reședință`, dacă e cazul.
8. **se copiază textul din Writer în Calc ca _text neformatat_, într-un tab nou, alături de cel cu sate**.  
9. se adaugă în Calc o nouă coloană numită `statut`, unde se completează cuvîntul `cătun` pentru fiecare rînd.
10. ștergem rîndurile cu comune care nu au cătune.