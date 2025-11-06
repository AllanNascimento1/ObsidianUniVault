\- \- \- [[2025-09-11]] \- \- \-
#### Ubuntu
Ubuntu è la versione di linux che usiamo in laboratorio

Usare questo commando su ubuntu: 
`sudo apt-get install build-essencial 

Editor per scrivere codice da comand shell in ubunto : pico
#### [[Linux Filesystem]]
Come ad Windows tutti i file del sistema operativo è organizzato con delle cartelle che creano un schema ad albero gerarchico, tutti i dati del sistema è salvato dentro la root che è la cartella iniziale che è rappresentata da " / ".
#### Permessi
Read - r
Write - w
Execute - x
#### Variabili
##### Globali
PATH   : Memorizza i percorsi dove sono contenuti i file eseguiti dei comandi. 
?   : Memorizza il codice di uscita del ultimo file eseguito.
##### Di Sessione
#### Comandi Linux
I comandi sono le prime lettere che dicono cosa fare e possono essere seguiti da dei **parametri/opzioni** per specificare dove applicare il comando e come.
Il sistema cerca questi comandi attraverso una variabile globale(?) chiamata PATH che indica le cartelle da cercare per trovare il file eseguibile del comando che hai indicato, le cartelle vengono cercate nel ordine indicato da " echo $PATH " e di conseguenza se un comando si trova nel ultima cartella il sistema può metterci un po per trovare il comando indicato.
La string di PATH è scritta " /usr/bin:/"

##### Lista Comandi Linux
cd  \<d\>  : ???
cd -   : Torna nella cartella iniziale (di solito la cartella del utente attuale).
ls /nomeDir   : Stampa tutti i file e cartelle dalla cartella indicata.
ls   : Stampa tutti i file e cartelle direttamente accessibili dal percorso attuale.
mkdir nomeDir   : Crea un nuovo percorso (Directory).
rm  nomeFile   : Cancella il file indicato.
cat  nomeFile   : Concatena file.
clear   : Cancella quello che hai scritto nella shell
man   : Manual
cp \<f1\> \<f2\>   : Copia file1 al file2
mv \<f1\> \<f2\>   : Muove file1 al file2
touch \<f\>  : Crea un file vuoto
exit   : Chiude il terminale
pwd   : Print working directory
type nomeComando   : Stampa il tipo del comando indicato. 
echo $nomeVar   : Stampa il valore della variabile indicata.
ll nomeFile   : Stampa i permessi del file per ogni utente o gruppo utenti.
\tmp   : Ritorna il percorso della cartella temporanea (non sempre)
##### Lista Opzioni Generali
./   : Cartella attuale.
\<f\>   : Indica un file.
\<d\>   : Indica una directory

#### Compilazione e esecuzione codice da linux
Per compilare un programma C++ su linux puoi usare il commando:
	g++ file.cpp
Questo commando creerà un file di nome a.out, che può essere eseguito attraverso il commando:
	./a.out
Questo significa che vuoi eseguire il file nella cartella ./ (quella attuale), se vuoi eseguire un file in un altra cartella puoi specificare il suo percorso invece di scrivere ./
