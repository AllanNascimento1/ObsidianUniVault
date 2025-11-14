Le variabili sono spazi di memoria composti da 4 componenti:
nome, tipo, locazione in memoria e il suo valore.
### Definizione 
Il compilatore alloca un area di memoria in grado di contenere la variabile con il tipo scelto.
Formato : tipo identificatore;

Si può definire e inizializzare una variabile nel stesso momento:
Formato : tipo identificatore = espressione;

**Inizializzare** una variabile è quando si assegna un valore ad essa per la prima volta, sovrascrivendo il valore sconosciuto che aveva nella sua definizione.

In C++ l'inizializzazione di una variabile deve sempre avvenire in qualche parte del codice prima di utilizzarla.
### Dichiarazione
Il compilatore specifica il tipo della variabile ma non alloca un spazio in memoria per essa, dunque spera che la variabile sia definita dopo nel codice.
Formato : extern tipo identificatore;

Variabili statiche sono variabili che ???
Le variabili globali nel multithreading vengono copiate per ogni istanza, quindi sono inefficienti nel caso del multithreading.