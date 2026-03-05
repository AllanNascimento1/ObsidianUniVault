I Linguaggi di programmazione sono divisi in 2 tipi diversi:
- Imperative (Imperativo) : 
	- Procedurale: C
	- Object Orientated Programming: Java
	- Scripting: Javascript
- Declarative (Dichiarativo) : 
	- Logica : Prolog
	- Funzionale : ML
## Programmazione Funzionale
La programmazione funzionale è un stile di scrittura di codice che mira a lavorare con i dati principalmente attraverso funzioni implementate a parte, questo stile di scrittura ha le seguente caratteristiche:
**Ricorsione** invece di iterazione :
	No cicli while o for.
**Pattern Matching** nei valori : 
	Se una riga di codice formata da una funzione e il suo parametro soddisfano un pattern già stabilito un valore specificato verrà ritornato.
**Espressioni** invece di statements : 
	Espressioni ottengono il risultato ottenendo i dati attraverso funzioni, mentre statements memorizzano i dati in variabili che saranno modificate.
**Funzioni** da per tutto :
	Funzioni e i suoi parametri sono usati per ottenere i risultati, funzioni possono anche essere passate come parametro ad altre funzioni.
#### Alcune Conseguenze
La programmazione funzionale non ha stati da modificare o dati esterni alle funzioni che possono essere modificati al di fuori dei dati che ritornano, questo limita cosa si può fare ma riduce significamente gli errori che può restituire il programma.

### Linguaggio ML
In questo corso vedremmo il linguaggio di programmazione funzionale ML, le sue caratteriste sono quelle descritte sopra per i linguaggi funzionali però ha alcune altre caratteriste specifiche: 
Strong typing cioè i tipi delle variabili sono determinati a compile time.
Polimorfismo, un tipo può assumere un valore di tipo derivato a se stesso.
Abstract data Types, permette la definizione di tipi nuovi.
#### Come eseguire un file ML:
Da command shell scrivi "poly" per entrare nel ambiente e successivamente scrivi il nome del file da eseguire. Per uscire dal ambiente poly usare "Ctrl+D" o per interromperlo usare "Ctrl+C".
#### Espressioni e Comandi
Espressioni sono entità che valutano un valore o non finiscono, sono composti da un simbolo/simboli e dagli argomenti, hanno tre tipi di notazione:
Infix : a +b 
Prefix : + a b
Suffix : a b +
Le espressioni possono essere valutate in 2 modi:
eager evaluation : valuta tutto (usato da ML).
lazy evaluation : valuta solo se necessario.

Comandi sono entità che modificano l'stato del programma, possono ritornare un valore o no, non esistono in linguaggi funzionali.
### Tipi Dato
Un tipo dato è una collezione di descrizioni di un insieme di valori e definisce gli operandi che possono essere applicati a questi valori.
### Type Systems
Un linguaggio può fare il controllo degli **errori di tipo** in due modi:
- **Static type checking** : controlla gli errori a compile time
- **Dynamic type checking** : controlla gli errori durante l'esecuzione
ML implementa il static type check ed è **strongly typed**, cioè le operazioni hanno bisogno di ricevere operandi del esatto tipo definito nella sua dichiarazione al contrario dei linguaggi **weakly typed** che per esempio accettano la divisione tra un numero intero e uno reale.
