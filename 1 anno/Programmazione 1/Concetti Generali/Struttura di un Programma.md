# Gestione memoria
L'area dedicata a un programma durante l'esecuzione è suddivisa in pezzi, i cui i più importanti sono:
#### Area Programma
Contiene le istruzione, in linguaggio macchina, del programma.
#### Area Stack
Contiene le variabili locali e i parametri formali delle funzioni.
#### Area dati Statici
Contiene le variabili globali , statiche e le costanti.
#### Area Heap
Contiene le variabili definite dinamicamente, cioè attraverso il costrutto new.
# Definizione di un Oggetto
Un oggetto (variabile, costante, tipo, funzione, ecc) ha tre caratteristiche al interno del programma: **Scope/Ambito** , **Visibilità** , **Durata** 
## Scope
L'ambito di un oggetto è la porzione di codice dove l'oggetto è definito, può essere **Globale** (definito nel file) o **Locale** (definito localmente).
## Visibilità
La visibilità di un oggetto stabilisce a quali punti nel codice è possibile accedere al oggetto, le funzioni e i blocchi annidati modificano la visibilità degli ogetti :
**Per le Funzioni**: Definizioni globali sono visibili dal interno, ma non viceversa. 
	Una definizione omonima nasconde una definizione globale.
**Per i Blocchi Annidati**: Definizioni esterne sono visibili dal interno, ma non viceversa. 
	Una definizione omonima nasconde una definizione globale.
## Durata
Stabilisce per quanto tempo un oggetto rimane allocato in memoria, gli oggetti possono essere dichiarati:
**Globale o Statico**: Dura fino alla fine del programma, usa l'area dati statici.
**Locale o automatico**: Dura solo fino alla fine del blocco dove è definito, usa l'area stack.
**Dinamico**: Dura fino che sono deallocati con il delete, usa l'area heap.
# Specificatori
Gli specificatori cambiano la definizione di un oggetto, cioè la durata, visibilità e scope.
## In C++
### Static
L'especificatore static forza la durata della variabile oltre la durata della funzione dove è definita, cioè il suo valore viene ricordato da una chiama a quella successiva.
La variabile è allocata nel area dati statici e viene inizializzata solo una volta al inizializzazione del programma.
Se applicato nel scopo **Globale** ha l'effetto di restringere la visibilità del oggetto al solo file dove è definito e non a altri eventuali file nella programmazione su più file.
### Extern
L'especificatore extern permette di dichiarare (cioè senza l'inizializzazione) un oggetto in un file che sarà definito (inizializzato o nel caso di una funzione assegnato il codice) in un altro file diverso.
