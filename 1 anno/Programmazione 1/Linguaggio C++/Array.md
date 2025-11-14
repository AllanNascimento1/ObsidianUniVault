# Array multidimensionali
## Statici
Gli array multidimensionali statici sono matrici dove tutte le loro dimensioni sono definite a compile time.

Dato che essi sono definiti a compile time, il compilatore può dedicare tutto l'spazio di memoria necessario in modo da avere tutti gli elementi della matrice uno dopo l'altro. In pratica questo significa che una matrice statica è come un array in memoria
### Definizione
`tipo ident[dim1][dim2]...[dimN];
NB: La definizione della matrice non significa che gli elementi saranno azzerati.
### Inizializzazione
`tipo ident[dim1][dim2] = {{1,2,3,...},{1,2,3,...},...}
NB: Quando viene fatta l'assegnazione a una matrice, tutti gli elementi non definiti dalla assegnazione saranno inizializzati a 0.
Esempio: `int mat[2][3] = {{3,3,3},{}} // valMat={{3,3,3},{0,0,0}}
### Aritmetica dei Puntatori
Quando hai un puntatore e lo sommi a un numero intero, il puntatore si muove per puntare alla prossima cella di memoria, dove una cella di memoria è la quantità di byte necessari per il tipo a quale punta. Questo significa che l'operazione:
`tipo* id=&var;
`id+=2; // Il compilatore lo interpreta: id=id+(2)*(sizeof(tipo))

Una variabile array equivale a una variabile puntatore costante. 
`int mat[5];  //= const int* mat;

Quindi l'operazione di prelevare un elemento del array equivale a scrivere:
`int var = mat[10]; //int var = *(mat+10)
### Utilizzo nelle Funzioni
#### Passaggio come parametro
Dato che gli array sono in pratica dei puntatori costanti, le seguenti definizioni sono interscambiabili:
`int func(int[dim]);
`int func(int[]);
`int func(const int*);
Se invece devi passare una matrice, le dimensioni superiori devono essere definite nel parametro:
`int func(int[dim1][dim2][dim3]);
`int func(int[][dim2][dim3]);
`int func(const int*[dim2][dim3]);
#### Ritorno di un Array
Una funzione normalmente non può ritornare un array, ma può ritornare se l'array è stato allocato esternamente alla funzione. Quindi può ritornare solo array passati da parametro, o definite globalmente. 
Questo perché l'spazio occupato **nel Stack** dalle variabili dichiarate al interno di una funzione, viene liberato alla fine della funzione.