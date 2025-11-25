Sia $V$ un spazio vettoriale e $B=\{v_1,...,v_n\}$ una base (ordinata) di $V$. Un elemento $v\in V = \sum_{i=1}^{n} x_iv_i$ dove $x_i\in \Bbb R$ sono le coordinate di $v$ rispetto alla base ordinata $B$, cioè un vettore $\vec w\in V=(w_1,w_2,w_3,w_4)$ dove base di $V$ è uguale a $B=(v_1,v_2,v_3,v_4)$ ha coordinate uguali a $x=(x_1,x_2,x_3,x_4)$
Indicheremo con $T_B(v)$ la $n$-upla delle coordinate di $v$ rispetto alla base $B$, si può anche scrivere $v=(x_1,...,x_n)_B$ , infatti $v=(x_1,...,x_n)$ è sottinteso di essere nella base canonica di $\Bbb K$ . In generale al cambiare della base cambia anche le coordinate del stesso vettore. 
Esempio: 
$v=(10,6,8)$ , $B=\{b_1,b_2,b_3\}=\{(2,0,0),(0,2,0),(0,0,2)\}$ 
Allora $T_B(v)=(5,3,4)$ dato che $v=5b_1+3b_2+4b_3$
Si può anche scrivere $v=(5,3,4)_B$
# Proprietà 
Tutte le basi di un spazio vettoriale $V$ hanno lo stesso numero di vettori.
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
Dato che la funzione è biunivoca allora è anche invertibile $T_B^{-1}(x_1,...,x_n)=\sum_{i=1}^{n} x_ie_i=v$ , tutte le funzioni lineare biunivoche sono dette **Isomorfismo**