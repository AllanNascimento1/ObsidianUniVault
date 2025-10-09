Sono in Gruppo 1
Martedì 8:30 - 10:30
Giovedì 10:30 - 12:30
Non usare strutture di C++ negli esami se è scritto di non farlo
Esami Open Book

##### Tutorato
da Lunedì 29 settembre 2025
14:30  - 16:30
Aula A201
tutor.programmazione1.disi@unitn.it

Linguaggio di programmazione [C++](Linguaggio%20C++) 

\- \- \- 2025-09-10 \- \- \-
TEORIA

Coding
	è il processo di conversione di un insieme di istruzioni in linguaggio parlato a un insieme di istruzioni in un linguaggio comprensibile ad un computer

Programming
	è l'insieme dei passaggi necessari per passare da una richiesta in linguaggio parlato a un insieme di istruzioni in linguaggio parlato. 
	Programming è più complesso del coding e infatti comprende anche una parte importante di coding ma comprende anche altri fasi come Analisi, Testing, Development, Performance e ecc.

\- \- \- 2025-09-11 \- \- \-
LAB
[[Linux]]

\- \- \- 2025-09-12 \- \- \-
TEORIA
Attento a compilazioni multiple negli esercizi del prof se si usa Visual Studio.

Installare il Subsystem Linux su Windows :
https://learn.microsoft.com/en-us/windows/wsl/

## Compilazione e Linking di un file
Il codice è scritto in file di testo (chiamato **sorgente**) attraverso l'uso di un editor, la sorgente deve successivamente essere compilata in un file con un linguaggio leggibile dal computer attraverso il seguente processo:
Il file sorgente viene preso dal sistema operativo e tradotto in un **File Oggetto** dal compilatore.
	Commando Linux : 
	g++ -c prova.cc
	(Crea un file oggetto "a.o")
Il file oggetto viene dopo collegato alle librerie di sistema dal linker e cosi viene generato un file eseguibile. 
	Commando Linux:
	g++ a.o 
	Altrimenti per compilare e linkare il file:
	g++ file.cpp
	(Crea un file a.out)
Puoi chiedere al compilatore di segnalare anche gli warning con:
	g++ -Wall file.cpp

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
[Stream in C++](Linguaggio%20C++#Stream)
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

Spiegazione del implementazione di tutti i tipi in C++ su [Tipi Dato C++](Linguaggio%20C++#Tipi%20Dato) 
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
Sono dei tipi costruiti dai tipi fondamentali attraverso vari meccanismi, i costrutti principali per costruire questi tipi sono:
I **Riferimenti**
**Puntatori**
**Array**
**Strutture**
**Unioni**
**Classi**
### I Riferimenti
I riferimenti permettono di assegnare più nomi (variabili) alla stessa area di memoria, in modo che puoi modificare il valore di quel area di memoria utilizzando uno dei due riferimenti che hai creato. 
Sintassi:
`int var = 0;
`int &riferimento = var; //prende l'area di memoria di var
`riferimento = 3; //modifica anche il valore di var
Questa variabile ritornerà sempre il valore di `var 

Una variabile riferimento nella sua dichiarazione deve essere inizializzata e non è possibile ridefinire dove punta.
Non viene applicato nessun cast nella sua dichiarazione, quindi deve avere lo stesso tipo della variabile originale.
### Operatori sugli indirizzi
#### & (Address-of)
Ritorna l'indirizzo di memoria del espressione a cui viene applicato.
#### \* (Dereference)
Ritorna il valore al interno del indirizzo di memoria del espressione a cui viene applicato.
### I Puntatori
I puntatori sono delle variabili che hanno la funzione di gestire le aree di memoria di altre variabili, quindi come valore hanno indirizzi di memoria.
Sintassi:
`int *id_var;
I puntatori ritornano l'indirizzo di memoria del oggetto a cui punta.

Per assegnare loro un indirizzo di memoria si deve 

Devono SEMPRE puntare a un oggetto con il loro stesso tipo.
Dato che i puntatori gestiscono indirizzi di memoria, la memoria che viene a loro allocata è solo quella sufficiente per memorizzare il numero che indica l'indirizzo di memoria, e di conseguenza tutti i puntatori indipendenti dal loro tipo occupano lo stesso spazio in memoria.

jninfjnfgjnifgjnifgjnisfdjnisfdsfdjnisfd

Si può creare puntatori senza tipo con la sintassi : 
`void *puntatore
Dato che questi puntatori non hanno tipo 