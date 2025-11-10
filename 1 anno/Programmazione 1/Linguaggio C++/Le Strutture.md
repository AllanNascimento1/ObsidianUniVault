Le Strutture sono una collezione ordinata di dati, detti anche campi o membri, che hanno tipo, nome e valore diversi.

Una struttura è interpretata dal compilatore come un nuovo tipo che potrà essere assegnato alle variabili, ma vengono usati diversamente dai tipi fondamentali dato che non possono essere usati come oggetto unico, ma invece si deve manipolare i campi al interno della struttura.
## Uso nel Codice
#### Definizione
Una struttura viene definita nel seguente modo : 
`struct nomeStrut{
`	tipo campo1;
`	...
`	tipo campoN;
`};
`nomeStrut var;

Si può creare strutture annidate, cioè con un o più campi che hanno il tipo definito da un'altra struttura.

Puoi anche definire dei costruttori alle strutture;
`struct esempio{
`	int campo1;
`	char campo2;
`	esempio() {};
`	esempio(int c1, char c2) {campo1 = c1; campo2 = c2;};
`};
#### Inizializzazione e Assegnazione
Possiamo inizializzare/assegnare la variabile con un valore nel seguente modo:
`struct persona{
`	char[] nome; 
`	int eta;
`};
`persona p1 = {"Erin Mujaj", 19};
I valori devono essere mesi in ordine, inoltre i campi senza valore saranno inizializzati a 0 se possibile.

Possiamo assegnare il valore di una struttura a un altra : 
`persona x,y = {"Furli", 19};
`x = y;
Ma la assegnazione viene fatta copiando ogni campo della struttura, il che può essere computazionalmente oneroso.
Anche i campi di tipo array statico vengono copiati elemento per elemento, causa principale delle basse prestazione di una copia di strutture.

Per assegnare ad una variabile di tipo puntatore una **Struttura Dinamica**:
`struct strutt{
`	int val;
`	char val2;
`};
`strutt* var = new strutt{5,'A'};

#### Accesso ai suoi campi
Per accedere ai campi di una struttura:
`nomeStrutt.nomeCampo;
Questa istruzione è dotata di indirizzo e quindi viene letta come un'altra qualsiasi variabile, cioè permette di passarla per riferimento o essere letta da << e >>.

Se ho un puntatore a una variabile di tipo struttura posso usare l'istruzione -> per ottenere il campo :
`nomeSrutt* idStrutt;
`idStrutt->campo1; // identico a (*idStrutt).campo1;
#### Passaggio di strutture alle funzioni
Come detto prima le strutture possono essere copiate, quindi al contrario degli array le strutture possono essere passate per valore alle funzioni e restituite tramite `return`, entrambi questi casi comportano una copia della struttura.
Dato che la copia delle strutture sono pesanti è preferibile **passare le Strutture per riferimento** facendo uso del `const` se servono solo per lettura.
#### Array come campi
Per creare un **Array Statico** come campo di una struttura basta crearlo con una dimensione fissa, mentre se vuoi creare un **Array Dinamico** dovrai creare la struttura con tipo puntatore e successivamente assegnare al campo  `new tipo[dim]`. 
Osservazione : Se il campo è un array dinamico allora sarà copiato solo il puntatore.
#### Strutture Ricorsive
È possibile creare una struttura ricorsiva se uno dei campi è un puntatore alla stessa struttura : 
`struct S{
`	int value;
`	S* next;
`};
NB: il campo DEVE essere un puntatore.
Esistono anche le strutture mutualmente ricorsive, ma dovrai dichiarare una delle strutture e definirla dopo.
`struct S2;
`struct S1{
`	int val;
`	S2* next;
`};
`struct S2{
`	int val;
`	S1* next;
`};
NB: Se non la dichiari S2 prima della definizione di S1 il compilatore segna un errore.
## Array di Strutture
Uno dei usi più comuni delle strutture è quello di gestire archivi ordinati di oggetti complessi attraverso una struttura dinamica (o array) di strutture che definiscono l'oggetto. 
Le strutture al interno del archivio vengono ordinate in base a uno dei suoi campi, che viene chiamato **chiave**, questo campo può essere per esempio : Una stringa che viene ordinata al interno del array in base al ordine alfabetico del suo primo carattere o Un numero ordinato in modo crescente.

Per la gestione del archivio ordinato spesso viene implementato delle funzioni per la aggiunta/rimozione degli elementi al archivio in modo da mantenere l'ordine, e per la ricerca di elementi nel archivio ordinato.
