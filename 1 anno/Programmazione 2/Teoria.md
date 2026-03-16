### V_Table
Tutti gli oggetti inizializzati in Java ereditano hanno un attributo "nascosto" chiamato **V_Table**, questo attributo è un array di puntatori che puntano ai metodi della classe che viene definita dalla sua V_Table dedicata. 
NB : I costruttori non fanno parte del comportamento della classe e di conseguenza non sono mesi nella V_Table.
Le V_Table sono costruite mettendo prima i metodi della super classe e dopo i metodi della classe stessa, questo perché semplifica il lavoro del compilatore nel trovare dove sono i metodi della super classe. 

I metodi in una V_Table sono ottenuti dalla sua posizione nel array, questa posizione resta costante per tutte le classe che ereditano questo metodo. Cioè se un metodo di una classe è nella posizione 4 nella V_Table esso sarà sempre nella posizione 4 anche su tutte le V_Table delle sue sotto classi. 
Questo comportamento ci permette anche di creare definizioni di metodi ereditati specifici a ogni classe, dato che il metodo avrà sempre la stessa posizione allora basta cambiare il puntatore in quella cella.
### Memoria
La memoria durante runtime di un programma Java ha 4 aree:
- Stack
- Heap
- Read Only Memory
- Code Section
Quando il programma inizia tutti i metodi e costruttori delle diverse classi nel programma vengono caricati nella Code Section della memoria, successivamente vengono create le V_Table delle diversi classi nella Read Only Memory.
Quando un oggetto viene creato una zona di memoria nella heap viene allocata per i suoi attributi+puntatore alla V_Table e nel stack viene memorizzato un puntatore alla sua area heap, in questo modo tramite il puntatore nel stack l'oggetto può accedere a tutti i suoi attributi e a tutti i suoi metodi usando la V_Table.
## Classi Astratte
Classi astratte non possono stanziare oggetti dato che (in teoria) hanno metodi astratti senza un corpo, cioè senza funzionalità, e di conseguenza il compilatore non sa cosa fare nel caso questi metodi vengano chiamati.
Per questo motivo tutti i metodi astratti ereditati **devono** essere definiti dalla classe che li ha ereditato.
Le classi astratte non hanno una V_Table.
