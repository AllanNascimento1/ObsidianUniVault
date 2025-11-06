Sono in Gruppo 1
Martedì 8:30 - 10:30
Giovedì 10:30 - 12:30
Esami Open Book
##### Tutorato
tutor.programmazione1.disi@unitn.it
## Link agli argomenti : 
[[Terminologia]]
[C++](Linguaggio%20C++.md) 
[[Linux]]
## Compilazione e Linking di un file

Invece per compilare un progetto diviso in più file il compilatore traduce uno alla volta tutti i file in file oggetti.
Dopo prende il file oggetti e li collega alle librerie di sistema dal linker e genera un singolo file eseguibile (default a.out)
	Comando Linux : 
	g++ prova1.cpp prova2.cpp . . . provaN.cpp

Nel file oggetto creato dal compilatore senza il linker è presente solo il codice a linguaggio macchina del file sorgente, quindi non è possibile compilarlo dato che non possiede ne il codice delle librerie di sistema ne il codice necessario per inserire il codice in memoria ed eseguirlo.

Il compilatore ha anche il compito di controllare se il codice contiene degli errori di sintassi ma NON errori a run time.

## Scrittura di un Programma
Identificatori : i nomi in un codice C++ devono essere univoci (per le variabili).
Parole Chiave : insieme di lettere che hanno già un significato stabilito dal linguaggio.
Espressioni Letterali : valori costanti (es: 40).

Sequenze di Escape :
\n   - Nuova riga
\t    - Tabulazione orizzontale
\v   - Tabulazione verticale
\b   - 
\f
\a
\\\
\\'
\\"

In C++ puoi cambiare la base di un numero : 
Decimale : 12
Esadecimale : 012 
Ottale : 0X12

\- \- \- 2025-09-17 \- \- \-
## Variabili e Costanti
Le variabili sono spazi di memoria composti da 4 componenti:
nome, tipo, locazione in memoria e il suo valore.
### Definizione 
Il compilatore alloca un area di memoria in grado di contenere la variabile con il tipo scelto.
Formato : tipo identificatore;

Si può definire e inizializzare una variabile nel stesso momento:
Formato : tipo identificatore = espressione;

**Inizializzare** una variabile è quando si assegna un valore ad essa per la prima volta, sovrascrivendo il valore sconosciuto che aveva nella sua definizione.

In C++ l'inizializzazione di una variabile deve sempre avvenire in qualche parte del codice prima di utilizzarla.
### Dichiarazione
Il compilatore specifica il tipo della variabile ma non alloca un spazio in memoria per essa, dunque spera che la variabile sia definita dopo nel codice.
Formato : extern tipo identificatore;

Variabili statiche sono variabili che ???
Le variabili globali nel multithreading vengono copiate per ogni istanza, quindi sono inefficienti nel caso del multithreading.
## Stream
Un programma comunica con l'esterno tramite uno o più flussi di caratteri chiamato stream. Un stream è una struttura logica costituita da una sequenza di caratteri, in numero teoricamente infinito, terminante con un apposito carattere che ne identifica la fine.
Gli stream vengono associati (con opportuni comandi) ai dispositivi fisici collegati al computer (tastiera, video) o a file residenti sulla memoria di massa (Hard disk).
[Stream in C++](Linguaggio%20C++.md#Stream)
## Tipi dato 
Variabili sono definite in parte dal loro tipo, questo è una categorizzazione delle variabili e stabilisce lo spazio che occupano in memoria, come sono codificate infine quali e come le operazioni possono essere fatte su di esse.
### Tipi dato numerici
I primi tipi dato da vedere sono quelli che gestiscono numeri, ci sono diversi tipi dato per gestire i numeri:
1. Interi positivi
2. Interi con segno
3. Numeri reali
Nei pc tutto (incluso i numeri) è rappresentato in memoria attraverso una sequenza di bit, che sono i zero e uno (hai studiato questo per 3 anni).

I **Tipi Interi positivi** usano tutti i bit nella sequenza per rappresentare il loro valore.

I **Tipi Interi con segno** sono rappresentati in due maniere:
	Segno-valore
La prima rappresentazione usa il bit più significativo (quello più a sinistra) come il segno. Questo sistema è poco usato dato che si deve gestire le operazioni di somma e moltiplicazione in due maniere diverse in base al segno della variabile.
	Complemento a 2
Il complemento a 2 è di gran lunga più diffuso dato che semplifica le operazioni, come la rappresentazione segno-valore il bit più significativo rappresenta il segno (0 positivo, 1 negativo) ma questo avviene perché il numero negativo è ottenuto nel seguente modo:
Si prende il numero positivo es:9 (00001001), si invertono i bit (11110110) e per fine si aggiunge uno es:-9 (11110111).

I **Numeri Reali** sono rappresentati attraverso l'standard IEEE 754, questo standard memorizza i numeri reali in notazione scientifica e di conseguenza è composto di alcune parte: Segno (+ o -) , Esponente , Mantissa e Offset
Esempi di notazioni scientifiche
Decimale : $131.1 = 1.321*10^2$ 
Binale : 
	9.25  $1001.01=1*1.00101*2^{3}$ 
	-0.75  $0.11=-1*1.1*2^{-1}$ 

Spiegazione del implementazione di tutti i tipi in C++ su [Tipi Dato C++](Linguaggio%20C++.md#Tipi%20Dato) 
## Istruzioni
**Istruzioni semplici** sono definizioni e espressioni che terminano in un punto virgola.
**Istruzioni strutturate** cambiano il flusso del programma, che di solito è sequenziale (riga per riga), permettendo azioni più complesse, possono essere :
	**istruzione composta**
	**istruzione condizionale**
	**istruzione iterative**
	**istruzione di salto**
### Composta
Non sembrano utili.
### Condizionale
**`if / if-else / switch`**
	Gli `if`, `if-else` e `switch` eseguono dei pezzi di codice in base a una condizione.
### Iterative
**`while / do-while / for`**
	I cicli invece ripetono un pezzo di codice finché una condizione non ritorni falso.
### Salto
**`break / continue / goto`**
	Queste istruzioni rompono il normale flusso del codice, facendo "saltare" la linea di codice da eseguire. Creano molta confusione quando si legge il codice quindi dovrebbero essere usata solo in casi ultra specifici.
## I Tipi derivati
Sono dei tipi costruiti dai tipi fondamentali attraverso vari meccanismi, i costrutti principali per costruire i tipi derivati tipi sono:
I **Riferimenti**
**Puntatori**
**Array**
**Strutture**
**Unioni**
**Classi**

Ogni Linguaggio di programmazione implementa diversamente questi costrutti, in [C++](Linguaggio%20C++.md#Tipi%20Derivati) tutti questi costrutti possono essere usati dal programmatore.
## Array

### Array multidimensionali
#### Statici
Gli array multidimensionali statici sono matrici dove tutte le loro dimensioni sono definite a compile time.

Dato che essi sono definiti a compile time, il compilatore può dedicare tutto l'spazio di memoria necessario in modo da avere tutti gli elementi della matrice uno dopo l'altro. In pratica questo significa che una matrice statica è come un array in memoria

**Definizione:**
`tipo ident[dim1][dim2]...[dimN];
NB: La definizione della matrice non significa che gli elementi saranno azzerati.

**Inizializzazione:**
`tipo ident[dim1][dim2] = {{1,2,3,...},{1,2,3,...},...}
NB: Quando viene fatta l'assegnazione a una matrice, tutti gli elementi non definiti dalla assegnazione saranno inizializzati a 0.
Esempio: `int mat[2][3] = {{3,3,3},{}} // valMat={{3,3,3},{0,0,0}}

**Aritmetica dei Puntatori**
Quando hai un puntatore e lo sommi a un numero intero, il puntatore si muove per puntare alla prossima cella di memoria, dove una cella di memoria è la quantità di byte necessari per il tipo a quale punta. Questo significa che l'operazione:
`tipo* id=&var;
`id+=2; // Il compilatore lo interpreta: id=id+(2)*(sizeof(tipo))

Una variabile array equivale a una variabile puntatore costante. 
`int mat[5];  //= const int* mat;

Quindi l'operazione di prelevare un elemento del array equivale a scrivere:
`int var = mat[10]; //int var = *(mat+10)

### Array/Matrici e funzioni
#### Array/Matrici statiche
**Passaggio come parametro**
Dato che gli array sono in pratica dei puntatori costanti, le seguenti definizioni sono interscambiabili:
`int func(int[dim]);
`int func(int[]);
`int func(const int*);
Se invece devi passare una matrice, le dimensioni superiori devono essere definite nel parametro:
`int func(int[dim1][dim2][dim3]);
`int func(int[][dim2][dim3]);
`int func(const int*[dim2][dim3]);

**Ritorno di un Array**
Una funzione normalmente non può ritornare un array, ma può ritornare se l'array è stato allocato esternamente alla funzione. Quindi può ritornare solo array passati da parametro, o definite globalmente. 
Questo perché l'spazio occupato dalle variabili dichiarate al interno di una funzione, viene liberato alla fine della funzione.
