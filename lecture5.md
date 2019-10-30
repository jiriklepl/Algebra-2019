## Grupy

Priklady 4.4:
1) G, H grupy, pak f: G -> H, kde f(g) = 1 pro kazde $g \in G$ je homomorfismus; Ker f = G
2) at T je teleso; U, V vektorove prostory nad T. Pak kazde linearni zobrazeni f: U -> V je homomorfismus grup U(+) a V(+)
3) pro grupu $S_n$ permutaci nad 1 az n uvazujeme zobrazeni sgn $S_n -> \{-1, 1\} (=Z(\cdot)^*)$, je homomorfismus grup, ktery surjektivni pro n > 1. Pak $Ker\ sgn =: A_n = \{\sigma \in S_n; \sigma \text{ suda}, sgn \sigma = 1\}$.

    - Lze ukazat. ze jedine normalni podgrupy $S_n$ pro $n \neq 4$ jsou prave $S_n, \{id\}, A_n$.


Znaceni:
    - $G(\cdot)$ grupa, $H, K \subseteq$ podmnoziny
    - $H \cdot K := \{hk; h \in H, k \in K\}$

Pozn.: Prestoze H, K mohou byt grupy v Gm nemusi HK byt nutne podgrupad, je-li $H \leq G$, pak gH, resp Hg se nazyva leva, resp prava rozkladna trida grupy G.


Poznamka 4.5: at G(.) je grupa, $H \leq G$, pak plati:
1)  $(a, b) \in rmod H \Leftrightarrow  (a^{-1}, b^{-1}) \in lmod H$
2) $|G / lmod H| = |G / rmod H|
3) $[a]_{lmod H} = aH, [a]_{rmod H} = Ha
4) $|[a]_{lmod H}| = |[a]_{rmod H} = |H|$

Dk:
1) $(a, b) \in rmof H \Leftrightarrow ab^{-1} \in H \Leftrightarrow (ab^{-1})^{-1} \in H \Leftrightarrow b a^{-1} \in H \Leftrightarrow (a^{-1}, b^{-1}) \in lmod H$
2) Z (1) plyne, ze $[a]_{lmod H} \rightarrow [a^{-1}]_{rmod H}$ je implikace neni mnozinami G / rmod H = G / lmod H.
3) Jen pro lmod H: $[a]_{lmod H} = \{b \in G; a^{-1} b \in H\} = \{b \in G; (\exists h \in H) a^{-1}b = h\} = \{b \in G; (\exists h \in H)b=ah\} = aH$
4) Z (3) staci najit, pro kazde $a \in G$, bijekci $H \rightarrow aH$, resp. $H \rightarrow Ha$ Takovymito bijekcemi jsou $L_a: H \rightarrow aH$ a $R_a: H \rightarrow Ha$ Zjevne jsou surjektivni a prostota plyne z kraceni.

Definice: G(.) je grupa:
- Radem G(.) rozumime |G|
- $[G : H] := |G / lmod H | = | G / rmod H |$ $\leftarrow$ to je index podgrupy H v G.

Veta 4.6 (Lagrangeova): Pro grupy G(.) a jeji podgrupu H plati:
- $|G| = |H| \cdot [G : H]$.

Dukaz:
- rmod H je ekvivalence na G.. $G = \bigcup\limits_{A \in G / rmod H} A \Rightarrow |G| = | \bigcup\limits_{A \in G / rmod H} A| =  \sum\limits_{A \in G / rmod H} |A|=  \sum\limits_{A \in G / rmod H} |H| =  |H|\cdot[G : H]$.

Dusledek 4.7: Rad podgrupy deli rad cele grupy (pro konecne grupy)
Priklady 4.8:
1) Je-li G grupa prvociselneho radu, pak {1}, G jsou jeji jedine podgrupy.
2) $|S_{10}| = 10$, $S_{10}$ neobsahuje podgrupy radu $11, 13,$ ani jenoho prvocisla $> 10$.
3) H, K dve konecne podgrupy G, kde $NSD(|H|. |K|) = 1$ pak $H \cap K = \{1\}$.


## Klasifikace cyklickych grup

Definice:
1) G(.) grupa, $X \subseteq G$ pak $<X>_G := \bigcap\limits_{X \subseteq H \leq G}H$... poodgrupa grupy G **generovana** X.
Misto $<\{g\}>_G$ budeme psat $<g>$.
2) grupa G(.) je **cyklicka**, existuje-li $g \in G$ ze $G = <g>_G$.
3) **Rad prvku g Grupy G(.)** je definovan jako rad grupy $<g>_G$

Priklad 5.1:
1) $\mathbb{Z}(+)$ je cyklicka grupa, jelikoz $\mathbb{Z} = <1>_\mathbb{Z}$.
2) Je-li $f : G \rightarrow H$ epimorfismus grup, kde G je cyklicka, tak H je take cyklicka.
    $G=<g>_G \Rightarrow H=<h>_H$
3) $\mathbb{Z}_n(+)$ je cyklicka, $\mathbb{Z}_n = <1>$.
     Tvrzeni: $NSD(n, a) = 1 \Leftrightarrow \mathbb{Z}_n = <a>$.
     Dk: $"\Rightarrow"$: ex. $b \in \mathbb{N}_0$, ze $1 = ba$ v $\mathbb{Z}_n$, tj. $1 == ba (mod n), 1 = ba + cn$ pro $c \in \mathbb{Z}$
     Pak $NSD(a,n)$ deli oba scitance vpravo $\Rightarrow NSD(a,n) | 1$.
     $"\Leftarrow"$: Z Bezoutovy rovnosti $b, c \in \mathbb{Z}$, ze $1 = ba + cn$, tj $1 === ba (mod n) \Leftrightarrow 1 === a (b mod n) (mod n) \Rightarrow 1 \in <a>_{\mathbb{Z}_n} \Rightarrow \mathbb{Z}_n = <a>_{\mathbb{Z}_n}$.

Znaceni: G(.) grupa $g \in G$.
- $g^0 := 1$, $g^n := g^{n-1}g$, pro $n \in \mathbb{N}$
- pro $n \in \mathbb{Z} \smallsetminus \mathbb{N}_0... g^{-n} := (g^{-1})^{|n|}$.
