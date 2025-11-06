Esistono alcuni standard (non officiali) che la maggior parte dei linguaggi di programmazione usano per leggere i file sorgenti, questi standard sono importanti perché sono la base di quasi tutti i linguaggi nei giorni d'oggi.
#### Identificatori
Gli identificatori sono tutti i nomi che il programmatore associa agli elementi del file sorgente, elementi come le variabili, funzioni, strutture e ecc. Questi nomi devono essere univoci al interno del loro **Contesto** e molti linguaggi sono **Case sensitive** cioè "var" è diverso da "Var".
#### Parole chiavi
Le parole chiavi sono tutte le parole e simboli che un linguaggio di programmazione ha già assegnato un significato fisso che non può essere cambiato dal programmatore, le parole chiavi sono usate per dire al compilatore cosa fare e non possono essere usate come identificatori.
### Rappresentazione del testo
Se vuoi usare testi al interno di un programma puoi farlo mettendolo dentro gli ' ' se è un singolo carattere e tra i "   " se è una stringa di caratteri. 
##### In C++
Per gestire alcuni casi di base esistono anche le **Sequenze di Escape** che cambiano come viene letto il testo dal PC : 
![[{C30E77C0-2BFB-4507-BD41-755DAD74E07E}.png]]
### Rappresentazione di numeri
I numeri vengono rappresentati da una sequenza di cifre, per i numeri con virgola molti linguaggi usano il punto (10.27).
##### In C++
In C++ puoi scrivere i numeri anche in base ottale mettendo un 0 davanti al numero, e in esadecimale mettendo 0X, questi numeri saranno tradotti a base decimale quando letti dal compilatore.
Puoi anche rappresentare i numeri attraverso la notazione scientifica se dopo un numero con virgola metti un "e" seguito dal esponente es: -1235.6e-2 = -12,356
### Operatori
Gli operatori nei linguaggi di programmazione sono tutti i caratteri speciali che denotano una certa operazione nel calcolo delle espressioni, quelli più comuni sono : 
`=  +  -  *  /  ||  &&  ==`
### Separatori
I separatori sono i caratteri speciali che denotano la fine di un istruzione o di un **Contesto**. Quelli più comuni sono: 
`() {} ;` 