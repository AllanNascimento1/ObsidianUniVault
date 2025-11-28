Sia $V$ un spazio vettoriale e $B=\{v_1,...,v_n\}$ una base (ordinata) di $V$. Un elemento $v\in V = \sum_{i=1}^{n} x_iv_i$ dove $x_i\in \Bbb R$ sono le coordinate di $v$ rispetto alla base ordinata $B$, cioè un vettore $\vec w\in V=(w_1,w_2,w_3,w_4)$ dove base di $V$ è uguale a $B=(v_1,v_2,v_3,v_4)$ ha coordinate uguali a $x=(x_1,x_2,x_3,x_4)$ dove $w_1=x_1v_1,w_2=x_2v_2,...$  
Indicheremo con $T_B(v)$ la $n$-upla delle coordinate di $v$ rispetto alla base $B$, si può anche scrivere $v=(x_1,...,x_n)_B$ , infatti $v=(x_1,...,x_n)$ è sottinteso di essere nella base canonica di $\Bbb K$ . In generale al cambiare della base cambia anche le coordinate del stesso vettore. 
Esempio: 
$v=(10,6,8)$ , $B=\{b_1,b_2,b_3\}=\{(2,0,0),(0,2,0),(0,0,2)\}$ 
Allora $T_B(v)=(5,3,4)$ dato che $v=5b_1+3b_2+4b_3$
Si può anche scrivere $v=(5,3,4)_B$
# Proprietà 
## Teorema della Base
Tutte le basi di un spazio vettoriale $V$ hanno lo stesso numero di vettori.
**Dimostrazione** : Per dimostrare tale teorema si possono usare le proposizioni 1,2 e 3 che in realtà sono definite nel spazio $\Bbb R^n$ e successivamente usare i teoremi 4 e 5 per associare tutti gli spazi vettoriali con campo in $\Bbb R$ al spazio $\Bbb R^n$.
## Proposizione 1
Se una base di $V$ ha $n$ vettori allora $m$ vettori, con $m>n$, sono sempre linearmente dipendenti.
## Proposizione 2
Se una base di $V$ ha $n$ vettori allora $n$ vettori linearmente indipendenti formano sempre una base di $V$
## Proposizione 3
Se una base di $V$ ha $n$ vettori allora $m$ vettori linearmente indipendenti, con $m<n$, possono sempre essere completati a una base di $V$ aggiungendo $m-n$ vettori.
### Completare base
Per completare $m$ vettori ($m<n$) per formare una base di $V$ consideri la matrice $M(n,m+n)$ dove le colonne sono gli $m$ vettori e gli $n$ elementi $e_1,...,e_n$ della base canonica di $V$, successivamente riduci la matrice agli scalini ridotti e la nuova base sarà formata dagli $m$ vettori più $m-n$ elementi della base canonica di $V$ trovati nelle ultime $n$ colonne della matrice ridotta, nelle colonne che contengono i pivot.
# Dimensione degli Spazi Vettoriali
Tutti gli spazi vettoriali $V$ sul campo $\Bbb K$ che possiedono una base $B=(e_1,...,e_n)$ possono associare a ogni vettore delle coordinate rispetto a $B$ attraverso la funzione $T_B$, queste coordinate sono un $n$-upla di elementi $k\in \Bbb K$, cioè $\Bbb K^n$. Grazie a questa corrispondenza tra gli spazi vettoriali e $\Bbb K^n$ possiamo dimostrare tutte le proprietà di $\Bbb K^n$ su gli altri spazi vettoriali.
## Proposizione 4
La funzione $T_B:V\rightarrow \Bbb K^n$ è iniettiva e suriettiva (biunivoca) e anche è lineare $T_B(a_1v_1+a_2v_2)$=$a_1T_B(v_1)+a_2T_B(v_2)$, per ogni $a_1,a_2\in \Bbb K$, $v_1,v_2\in V$.
Dato che la funzione è biunivoca allora essa è anche invertibile $T_B^{-1}(x_1,...,x_n)=\sum_{i=1}^{n} x_ie_i=v$ 
### Definizione 1: Isomorfismo
Tutte le funzioni lineare biunivoche sono dette **Isomorfismo**.
### Proposizione 5
I vettori $v_1,...,v_m$ di $V$ sono indipendenti (o generatori, o base) solo se le immagini $T_B(v_1),...,T_B(v_m)$ di $\Bbb K^n$ sono indipendenti (o generatori, o base di $\Bbb K^n$), dove $B$ la base canonica di $V$.
Per esempio puoi determinare la in/dipendenza lineare di polinomi in $\Bbb R_{n-1}[x]$ trasformandoli in vettori in $\Bbb K^n$ attraverso $T_B$ dove $B=\{x^{n-1},...,x,1\}$.
# Somma e intersezione di sottospazi
Dati due sottospazi $U,W$ di un spazio vettoriale $V$, l'intersezione tra $U\cap W$ è ancora un sottospazio, però l'unione $U\cup W$, in generale, non forma un spazio vettoriale dato che non rispetta il criterio della chiusura rispetto alla somma. 
Per questo motivo, tranne nel caso in cui $U$ e $W$ sono uguali formando cosi un sottospazio, l'unione non sarà trattata.
Al posto del unione consideriamo la somma $U+W$ che è ancora un sottospazio, questa somma contiene tutti i vettori che può essere espresso come somma tra i vettori di $U$ e $W$, è generato dal unione tra l'insiemi generatori di $U$ e $W$ (non confondere l'unione degli **Insiemi Generatori** con l'unione dei sottospazio $U$ e $W$).
$$U+W=\{v=u+w\in V|u\in U,w\in W \}$$
#### Formula di Grassmann
$$dim(U+W)+dim(U\cap W)=dim(U)+dim(W)$$
Questa formula funziona perché la dimensione della somma $U$ e $W$ è il numero di vettori **LI** nel unione tra gli insiemi generatori, mentre la dimensione del l'intercessione è il numero di vettori **LD** nella unione tra l'insiemi generatori. La somma dei numeri di vettori **LI** e **LD** è uguale al numero totale di vettori, cioè $dim(U)+dim(W)$.