# Teoria
Un programma comunica con l'esterno tramite uno o più flussi di caratteri chiamato stream. Un stream è una struttura logica costituita da una sequenza di caratteri, in numero teoricamente infinito, terminante con un apposito carattere che ne identifica la fine.
Gli stream vengono associati (con opportuni comandi) ai dispositivi fisici collegati al computer (tastiera, video) o a file residenti sulla memoria di massa (Hard disk).
# In C++
## Scrittura
Per scrivere dati dentro un stream si usa l'istruzione:
`stream << espressione1 << espressione2 << . . .;`

Questo si chiama **Scrittura Multipla** e equivale a scrivere:
`stream << espressione1`;
`stream << espressione2`;
## Lettura
`stream >> var;
Questa operazione ritorna vero se non ci sono stati errori nel assegnazione, altrimenti ritorna falso.
## Stream predefinite
### `<iostream>`
In C++ esistono i seguenti stream predefiniti:
`cin`   : Per prelevare caratteri o comandi dalla tastiera.
`cout`   : Per scrivere dati di uscita, tipicamente associato allo schermo.
`cerr`   : Per la gestione degli errori.
