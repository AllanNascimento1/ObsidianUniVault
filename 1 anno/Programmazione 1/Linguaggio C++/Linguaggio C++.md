[Basi per la scrittura di un programma](Scrittura%20di%20un%20Programma)
## Operatori 
Gli operatori in 
## Tipi dato
Sono distinti in:
**Tipi fondamentali** (informazioni semplici):
	**interi** : int, short, long, long long
	**boolean** : bool
	**enumerativi**: enum
	**carattere**: char
	**numeri reali**: float, double, long double
	
**Tipi derivati:**
	costruiti a partire dei tipi fondamentali mediante array, puntatori e ecc.

Puoi usare la funzione `sizeof(var)` per ottenere la loro dimensione in byte.
### Tipi Fondamentali
#### Interi
Tipicamente codificati a complemento a 2 (quindi con segno), la dimensione che occupano può cambiare da macchina a macchina. 
puoi creare interi positivi aggiungendo `unsigned` prima del tipo.

**Operazioni**
Le operazioni tra due numeri interi risulterà sempre in un numero intero, quindi per esempio se una divisione ritorna un numero con virgola essa sarà tagliata fuori.
Bit-a-bit :
\>> e <<   |   x>>n   |   shift di n bit 
&   |    x&y   |   AND bit a bit tra x e y
"|"   |   x|y   |   OR 
^   |   x^y   |   XOR
~   |   ~x   |   NOT

### Boolean
Tipo dato per gestire valori Vero=1 o Falso=0, usa la [[Logica Booleana]].
L'AND e OR sono valutati attraverso la lazy evaluation, quindi se non è necessario valutare tutta l'operazione il calcolatore salterà alcune espressioni.

#### Numeri Reali
Memorizza numeri reali, ricordarti che hanno una precisione limitata che può nel corso di diverse operazioni cambiare il risultato finale sostanzialmente.
Il confronto tra due reali può essere problematico. 
**Operazioni**
Le operazioni tra numeri reali, come negli integer, risulterà sempre in un numero reale.
#### Enumerativi
`enum typeid = {nomeEnum1, nomeEnum2, ...};`
Il nome del `enum` può anche essere sostituito da un numero intero, che lo identificherà e sarà il suo valore.
#### Caratteri
Usati per memorizzare una singola lettera o simbolo, dove ogni numero da 0 a 128 (un byte) viene associato ad una lettera o simbolo specifico, il simbolo al quale viene associato dipende dal formato usato dalla macchina, ma il formato più usato è ASCII.
Dato che i caratteri sono in realtà numeri interi, si può usare le operazioni degli interi sui caratteri. Esempio `'a'+3 = 'd'`
#### Operazioni miste e conversione 
Se un espressione ha un tipo intero e uno reale il risultato sarà reale, nel stesso modo se un operazione è fatta tra due numeri di dimensione diversa il risultato sarà del tipo di dimensione maggiore (`short + int = int`).

Questa trasformazione dei tipi si chiama **conversione** ed è sempre necessaria per le operazioni miste, la conversione può essere:
Implicita : Effettuata dal compilatore in automatico.
Esplicita : 
Effettuata dal programmatore attraverso i cast che possono essere:

**Down cast** se parte da un tipo grande a uno più piccolo, float a un int. In questo caso si perde sempre dati, nel caso da float a int si perde la virgola e quindi precisione.

**Up cast** se parte da un tipo piccolo a un numero grande.

Esiste anche il cast per tipi compatibili, es : char a int.
### Stream
In C++ esistono i seguenti stream predefiniti:
`cin`   : Per prelevare caratteri o comandi dalla tastiera.
`cout`   : Per scrivere dati di uscita, tipicamente associato allo schermo.
`cerr`   : Per la gestione degli errori.

La libreria che gestisce questi stream è \<iostream\>
Per scrivere dati dentro un stream si usa l'istruzione:
`stream << espressione1 << espressione2 << . . .;`

- Questo si chiama **Scrittura Multipla** e equivale a scrivere:
`stream << espressione1`;
`stream << espressione2`;
### Tipi Derivati
#### I Riferimenti
I riferimenti permettono di assegnare più nomi (variabili) alla stessa area di memoria, in modo che puoi modificare il valore di quel area di memoria utilizzando uno dei due riferimenti che hai creato. 
Sintassi:
`int var = 0;
`int &riferimento = var; //prende l'area di memoria di var
`riferimento = 3; //modifica anche il valore di var
Questa variabile ritornerà sempre il valore di `var`. 

NB: nella dichiarazione di una variabile riferimento si deve usare la variabile se stessa e non la sua area di memoria, quindi se vuoi usare un puntatore per dichiarare un riferimento dovrai prima usare il deference.
`int var = 0;
`int* id_var = &var;
`int& ref_var = *id_var;

Una variabile riferimento nella sua dichiarazione deve essere inizializzata e non è possibile ridefinire dove punta, in più la variabile riferimento **DEVE** avere lo stesso tipo della variabile.
#### Operatori sugli indirizzi
#### & (Address-of)
Ritorna l'indirizzo di memoria del espressione a cui viene applicato e serve anche per creare variabili reference.
#### \* (Dereference)
Ritorna il valore al interno del indirizzo di memoria del espressione a cui viene applicato, usato per i puntatori.
#### I Puntatori
I puntatori sono delle variabili che hanno la funzione di gestire le aree di memoria di altre variabili, quindi come valore hanno indirizzi di memoria.
Sintassi:
`int *id_var;
I puntatori ritornano l'indirizzo di memoria del oggetto a cui punta.

**Assegnazioni a Puntatori**
Per assegnare loro un indirizzo di memoria si deve fare uso del istruzione di **Address-of (&)**, che restituirà l'indirizzo di memoria del oggetto a cui è applicato.
`int *id_var;
`int var = 10;
`id_var = &var;  //&var restituisce il valore in memoria di var : 0x7ffe0be9a4ac

L'assegnazione tra puntatori è quando non usi nessun dei due operatori.
`int var0 = 10;
`int* var1 = &var0;
`int* var2;
`var2 = var1;  //var2->var0 e var1->var0

Un puntatore deve **SEMPRE** puntare a un oggetto con il suo stesso tipo.
Dato che i puntatori gestiscono indirizzi di memoria, la memoria che viene a loro allocata è solo quella sufficiente per memorizzare il numero che indica l'indirizzo di memoria, e di conseguenza tutti i puntatori indipendenti dal loro tipo occupano lo stesso spazio in memoria.

**Accedere ai Puntatori**
Per accedere al oggetto che il puntatore sta puntando si dovrà usare l'operazione di dereference "\*"
`int var = 10;
`int *id_var = &var;
`int test = *id_var + 1; //test= var+1 (10+1)
`*id_var = 12; //var=2

**Puntatori void**
Si può creare puntatori senza tipo con la sintassi : 
`void *puntatore
Dato che questi puntatori non hanno tipo si dovrà fare uso del cast esplicito per usarli.
`int var = 10;
`char let = 'a'
`void* idVar = &var;
`*(int*)idVar = 1; //var = 11
`idVar = &let;
`cout<<*(char*)idVar;  //stampa "a"

**Puntatori costanti**
Ci sono 3 tipi di puntatori costanti:
Puntatori a costante:
`const int* var;

## Allocazione e Deallocazione
### Statica
La allocazione di memoria statica obbliga a definire la struttura e la dimensione a compile time, dato che memorizza i dati nel stack. Un esempio di allocazione statica è la dichiarazione di un array statico, o semplicemente la dichiarazione di una variabile di tipo base (fondamentale).

### Dinamica
La allocazione dinamica usa un'area di memoria chiamata store (heap) che gestisce l'acceso a questi dati attraverso i puntatori.
Per la gestione dinamica della memoria in C++ esiste due operatori:
`new tipo` - Alloca un area nel heap adatta a contenere un oggetto della dimensione del suo tipo.
`new tipo[n]` - Alloca nel heap n celle della dimensione del tipo, ossia per memorizzare un array.
`delete indirizzo` - Dice al sistema operativo che quel area di memoria non è più utilizzata dal programma, i dati al interno del heap non vengono azzerati.
`delete[n] indirizzo` - Dice al SO di liberare le n celle di dimensione del tipo.

NB: quando uso `delete` a un'area di memoria, quella area può comunque essere accesa dal puntatore.

Attraverso la gestione dinamica della memoria possiamo introdurre [[Le Strutture]].
# Librerie
#### `<iostream>
#### `<fstream>
#### `<string>
#### `<ctime>
#### `<cstdlib>
#### `<cassert>
##### Funzioni:
`assert(bool) : lancia un errore se il parametro è falso
