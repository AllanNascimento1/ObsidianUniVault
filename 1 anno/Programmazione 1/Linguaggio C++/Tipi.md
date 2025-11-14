Le variabili di tipo fondamentale memorizzano informazioni semplici, in C++ 

Puoi usare la funzione `sizeof(var)` per ottenere la dimensione in byte del tipo della variabile.
# Teoria
Variabili sono definite in parte dal loro tipo, questo è una categorizzazione delle variabili e stabilisce lo spazio che occupano in memoria, come sono codificate infine quali e come le operazioni possono essere fatte su di esse.
## Tipi dato numerici
I primi tipi dato da vedere sono quelli che gestiscono numeri, ci sono diversi tipi dato per gestire i numeri:
1. Interi positivi
2. Interi con segno
3. Numeri reali
Nei pc tutto (incluso i numeri) è rappresentato in memoria attraverso una sequenza di bit, che sono i zero e uno.
### Interi
I **Tipi Interi positivi** usano tutti i bit nella sequenza per rappresentare il loro valore.

I **Tipi Interi con segno** sono rappresentati in due maniere:
	Segno-valore
La prima rappresentazione usa il bit più significativo (quello più a sinistra) come il segno. Questo sistema è poco usato dato che si deve gestire le operazioni di somma e moltiplicazione in due maniere diverse in base al segno della variabile.
	Complemento a 2
Il complemento a 2 è di gran lunga più diffuso dato che semplifica le operazioni, come la rappresentazione segno-valore il bit più significativo rappresenta il segno (0 positivo, 1 negativo) ma questo avviene perché il numero negativo è ottenuto nel seguente modo:
Si prende il numero positivo es:9 (00001001), si invertono i bit (11110110) e per fine si aggiunge uno es:-9 (11110111).
### Reali
I **Numeri Reali** sono rappresentati attraverso l'standard IEEE 754, questo standard memorizza i numeri reali in notazione scientifica e di conseguenza è composto di alcune parte: Segno (+ o -) , Esponente , Mantissa e Offset
Esempi di notazioni scientifiche
Decimale : $131.1 = 1.321*10^2$ 
Binale : 
	9.25  $1001.01=1*1.00101*2^{3}$ 
	-0.75  $0.11=-1*1.1*2^{-1}$ 
# Tipi in C++

In C++ una variabile può essere di Tipo Fondamentale oppure di Tipo Derivato.

I **Tipi Fondamentali** gestiscono le informazioni elementari di un programma cioè i numeri, caratteri e boolean. Sono divisi nei seguenti tipi:
**interi** : int, short, long, long long
**boolean** : bool
**enumerativi**: enum (interi costanti)
**carattere**: char
**numeri reali**: float, double, long double

I **Tipi Derivati** invece permettono un comportamento più complesso e flessibile di un programma dato che gestiscono un gruppo di informazioni elementari, infatti i tipi derivati sono formati dai tipi fondamentali attraverso vari meccanismi e costrutti.
I costrutti principali per costruire i tipi derivati tipi sono:
**Riferimenti**
**Puntatori**
**Array**
**[Strutture](Le%20Strutture)**
**[[Unioni]]**
**[[Classi]]**
## Tipi Fondamentali
### Interi
Tipicamente codificati a complemento a 2 (quindi con segno), la dimensione che occupano può cambiare da macchina a macchina. 
puoi creare interi positivi aggiungendo `unsigned` prima del tipo.
#### Operazioni
Le operazioni tra due numeri interi risulterà sempre in un numero intero, quindi per esempio se una divisione ritorna un numero con virgola essa sarà tagliata fuori.
##### Operazioni Bit-a-bit :
\>> oppure <<   |   x>>n   |   shift di n bit 
&   |    x&y   |   AND bit a bit tra x e y
"|"   |   x|y   |   OR 
^   |   x^y   |   XOR
~   |   ~x   |   NOT
### Boolean
Tipo dato per gestire valori Vero=1 o Falso=0, le operazioni sono definite dalla [[Logica Booleana]].
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
## Tipi Derivati
## I Riferimenti
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
## Operatori sugli indirizzi
#### & (Address-of)
Ritorna l'indirizzo di memoria del espressione a cui viene applicato e serve anche per creare variabili reference.
#### \* (Dereference)
Ritorna il valore al interno del indirizzo di memoria del espressione a cui viene applicato, usato per i puntatori.
## I Puntatori
I puntatori sono delle variabili che hanno la funzione di gestire le aree di memoria di altre variabili, quindi come valore hanno indirizzi di memoria.
Sintassi:
`int *id_var;
I puntatori ritornano l'indirizzo di memoria del oggetto a cui punta.
### Assegnazioni a Puntatori
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
