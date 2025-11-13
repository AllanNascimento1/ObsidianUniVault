Al contrario degli array standard, le liste concatenate sono una collezione di oggetti composta da elementi che non sono messi sequenzialmente nella memoria, ma invece ogni elemento contiene le informazioni necessarie per trovare l'elemento successivo.

`struct nodo{
	`int dato;
	`nodo* next;
`};

Gli elementi nelle liste concatenate sono chiamati **Nodi** che contengono sia l'oggetto sia un indirizzo al nodo successivo, il nodo finale di una lista è un caso di eccezione dato che non ha un nodo successivo da puntare quindi si può adottare alcune convenzioni :
- Punta a NULL.
- Punta a un nodo fittizio.
- Punta al primo nodo della lista.
### Operazioni
#### Calcolo Lunghezza
Esempio dove ultimo nodo punta a null :
`int listSize(nodo* head){
	`nodo* curNode = head;
	`int size = 0;
	`while(curNode != nullptr){
		`size++;
		`curNode = curNode->next;
	}
	`return size;
`}
- Inserimento Dato
- Cancellazione Dato

Attento nel implementazione quando devi rimuovere/aggiungere un nodo alla testa o alla coda della lista. 

- Rovesciamento di una lista
- Concatenazione di due liste

Controllare che viene passato un puntatore valido (non null) quando vuoi implementare queste operazioni.
**NB** : 
- Non dimenticarti di passare il primo nodo della lista **per Riferimento** alle funzioni che implementano queste operazioni, in modo da modificare a quale nodo punta la lista. Altrimenti corri il rischio di perdere la lista e creare memory leak.
- Se usi new per creare i nodi della lista **DEVI**, prima della fine del programma, de-allocare ogni nodo della lista con l'uso del `delete`. Quindi in pratica devi implementare una funzione che scorre la lista e de-alloca ogni elemento.