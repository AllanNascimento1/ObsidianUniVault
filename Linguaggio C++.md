### Tipi dato
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

#### Boolean
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