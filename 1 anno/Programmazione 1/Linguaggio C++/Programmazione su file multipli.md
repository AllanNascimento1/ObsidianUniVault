I programmi possono essere organizzati su più file, in modo da portarsi diversi vantaggi dal punto di vista organizzativo e anche al livello di prestazioni della compilazione.
Un modo per gestirsi l'organizzazione dei file in C++ è **l'organizzazione Modulare**, dove ogni file raggruppa un insieme di funzionalità (modulo), questo comporta una compilazione separata di ogni file e successivamente il linking del file oggetto generato.
## Moduli
In C++ di solito un programma separato su più file ha 2N + 1 file, dove N è il numero di moduli e il +1 è il main.cc.
Ogni modulo è formato da due file : Un file header (modulo.h) dove viene scritto i "header" delle funzioni del modulo, Un file sorgente (modulo.cc) dove viene assegnato le definizione delle funzione scritte nel header.
