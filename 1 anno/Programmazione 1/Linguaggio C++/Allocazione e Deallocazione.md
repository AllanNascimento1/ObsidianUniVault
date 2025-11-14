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