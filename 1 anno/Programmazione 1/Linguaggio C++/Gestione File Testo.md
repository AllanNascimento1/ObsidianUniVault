## Argomenti da linea di comando
Per facilitare l'uso di un programma si può configurare il main in modo che accetti il passaggio di parametri dal terminale. 
`int main(int argc, char* argv[])`
`argc` - Il numero di parole nella riga del terminale (quindi incluso anche il nome del file eseguibile a.out)
`argv` - Il contenuto di quello che è scritto nel terminale, es: 
`terminale#a.out test temp`
`argv[0]="a.out" , argv[1]="test" , argv[2]="temp"`

## `<fstream>
Per gestire la lettura/scrittura dei file.
### Costanti
### Oggetti
### Funzioni
input è una variabile di tipo `fstream`
`input.open(percFile, tipoFile)` - Apre la stream con il file, il primo parametro è il percorso del file
`input.get(c)`
`input.fail()` - 
`input.eof()` - EndOfFile : ritorna true se è il puntatore non punta a nessun carattere.