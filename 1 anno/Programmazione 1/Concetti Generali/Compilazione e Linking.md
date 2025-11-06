Il codice è scritto in file di testo (chiamato **Sorgente**) attraverso l'uso di un editor, la sorgente deve successivamente essere compilata in un file con un linguaggio leggibile dal computer.
#### Compilatore
Il compilatore prende un file sorgente scritto in un linguaggio di programmazione specifico e lo traduce in un **File Oggetto**, che dovrà successivamente passare dal linker per diventare un file eseguibile.

Nel file oggetto creato dal compilatore è presente solo il codice a linguaggio macchina del file sorgente, quindi non è possibile eseguirlo dato che non possiede ne il codice delle librerie di sistema ne il codice necessario per inserire il codice in memoria ed eseguirlo.

Il compilatore ha anche il compito di controllare se il codice contiene degli errori di sintassi ma NON errori a run time.
#### Linker
Successivamente viene fatto il linking del file oggetto attraverso il **Linker** che trasforma il file oggetto in un **File Eseguibile**, su Windows i file eseguibili hanno l'estensione .exe mentre su Linux .out 
#### Programma diviso in più file
La compilazione di un programma diviso in più file è un po' diversa da quella per un singolo file sorgente, prima tutti i file vengono tradotti in file oggetto dal compilatore come per i singoli file, però nella fase di linking il linker associa le librerie di sistema ai file oggetti e crea un unico file eseguibile con tutto il codice del programma.
## Compilazione e Linking su Ubuntu
Su ubuntu possiamo installare il compilatore g++ subito dal terminale attraverso il commando:
`sudo apt-get install build-essential
Questo è un compilatore per i file sorgenti scritti in C++, per compilare un file C++ attraverso il terminal puoi usare : 
`g++ -c prova.cc` - Crea un file "a.o" nella directory attuale (il -c è per compilare senza fare il linking dopo).
Ci sono alcuni parametri che puoi usare dopo g++ per cambiare le configurazioni per la compilazione del file : 
`g++ -Wall file.cpp` - Dice al compilatore di segnalare gli warning.

Per effettuare il linking su un file oggetto basta passarlo di nuovo sul commando g++
`g++ a.o` - Crea il file eseguibile "a.out"

Altrimenti per compilare e linkare il file nel stesso commando:
`g++ file.cpp` - Crea il file eseguibile "a.out"
### Programma diviso in più file
Per compilare un programma diviso in più file possiamo usare il commando :
`g++ file1.cpp file2.cpp . . . fileN.cpp` - Crea un singolo file eseguibile a.out

