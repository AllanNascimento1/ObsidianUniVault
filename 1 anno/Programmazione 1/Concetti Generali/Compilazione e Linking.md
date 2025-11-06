Il codice è scritto in file di testo (chiamato **sorgente**) attraverso l'uso di un editor, la sorgente deve successivamente essere compilata in un file con un linguaggio leggibile dal computer.
Il file sorgente viene preso dal sistema operativo e tradotto in un **File Oggetto** dal compilatore, questo file non è ancora eseguibile perché non è stato effettuato il **Linking** del file oggetto alle librerie e altri componenti necessari.
Successivamente viene fatto il linking del file oggetto che diventa un **File Eseguibile** dal sistema operativo, su Windows ha l'estensione .exe mentre su Linux .out 
### Compilazione e Linking su Ubuntu
Su ubuntu possiamo installare il compilatore g++ per la compilazione di file sorgenti scritti in C++, e successivamente compilarli da terminal attraverso : 
`g++ -c prova.cc` - che crea un file "a.o" nella directory attuale.
Ci sono alcuni parametri che puoi usare dopo g++ per cambiare le configurazioni per la compilazione del file : 
`g++ -Wall file.cpp` - Dice al compilatore di segnalare gli warning.

Per effettuare il linking su un file oggetto basta passarlo di nuovo sul commando g++
`g++ a.o` - Crea il file eseguibile "a.out"

Altrimenti per compilare e linkare il file nel stesso commando:
`g++ file.cpp` - Crea il file eseguibile "a.out"
