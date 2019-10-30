## Klasická čínská věta o zbytcích

Ať $n1, ...nk \in N \setminus \{1\}$, po dvou nesoudelna, $n := n1..nk$
Pak ma kazda soustava kongruenci $x === u_1 mod n1$, ... $x === uk mod n k$

dk: buno $u_i \in Z_{n_i} \forall i \in \{1..k\}.$, Z vety 2.5   najdeme $x = H^{-1}(u_1...u_k)$

---

definice at * je bin op na A, ~ je lin rel na A. rekneme ze ~ je slucutelna s *, pokud $\forall a_1,a_2,b_1,b_2 \in A: (a_1 ~ b_1 \wedge a_2 ~ b_2 \Rightarrow a_1 * a_2 ~ b_1 * b_2$.


Z pozn  2.6 plyne, ze relace $.===. (mod n)$ je slucitelna s +, -, *.


## Asociativni bin op

def: at A mnozina, * binop na A, ze e \in A je neutralni vzhledem k *, pokud $\forall a \in A: a * e = e * a = a$.

pozn 3.1 pokud neutralni prvek existuje, je urcen jednoznacne.

dk: at $ e,f \in A$ jsou neutr prvky (ruzne), pak $e  * f = e = f$. SPORRRRRRR

def: at * je binop na A. pak prvek $a \in A$ je invertibilni (vzhledem k *), pokud $\exists b \in A: a * b = b * a = e$, kde e je neutralni prvek.

def: 

1. at G  je mn, . je binop na G, pak G(.) je grupoid (magma).
2. . asociativni $\Rightarrow$ G(.) je pologrupa (subgroup)
3. pokud navic ma neutralni prvek, je to monoid
4. pokud je G(.) monoid a kazdy prvek je invertibilni, pak G(.) je grupa.
5. je-li v G(.) binop . komutativni, nazyvame G(.) komutativni -||-

pozn: komutativni grupa se nekdy nazyva abelovska grupa

pr 3.2: at $n \in N \ \{1\}$ a X mnozina, |X| > 1.

1. operaci * na X definujeme vztahem $x*y = x$, X(*) je pologrupa, ale neni monoid (nema el prvek) - ponauceni: overit neutralitu z vobou stran
2. at M(X) je mnozina vsech slov nad abecedou X, kde konkatenace je provedena pres .
    - . zjevne neni komutativni
    - muzeme oznacit prazdne slovo $\epsilon$ - to slouzi jako neutralni prvek
    - M(X)(.) je (slovni) monoid (- bez toho slova $\epsilon$ slovni grupoid)
3. $T(X) = \{f: X \rightarrow X; f \text{ zobrazeni}\}$ spolu s operaci $\circ$ skladani tvori tzv transformacni monoid (neutralni prvek je $id_X$)
    - napr pro $X = Z$ mame $\alpha,\beta$, kde $\alpha(k) = 2k, \beta(k) = \lfloor \frac{k}{2}\rfloor$ pak $\beta \circ \alpha = id_Z$ a $\alpha \circ \beta \neq id_Z$. Ponauceni: (V definici invertibilniho prvku nestaci uvazovat jen jednu z rovnosti)
4. $M_n(T)....$ mnozina nxn matic nat telesem T tvori spolu s operaci + grupu, spolu s . monoid.
5. $M_n(T)....$ mnozina nxn regularnich matic nat telesem T tvori spolu s . grupu.


---

pozn technicka: v dalsim, kdyz rekneme ze G(.) je monoid, budeme znacit neutralni prvek jako 1. + casto se tecka jen tak zbuhdarma vypousti pro prdel.

pozn 3.3: at G(.) je monoid, $a,b,,c \in G(.)$. predp ze $ab = ca = 1$, pak $b = c$ je jednoznacne urceny inverzi prvek k a a my ho budeme znacit: $a^{-1}$.

dk: mejme $cab$, pak z asociativity $b = (ca)b = cab = c(ab) = c$.


znaceni: G(.) monoid, pak $G* = \{a \in G: a \text{ je invertibilni}\}$


poznamka 3.4: necht G(.) je monoid, pak pro $s, t \in G*$: $st \in G*$, $(st)^{-1} = t^{-1} s^{-1}$ a $(s^{-1})^{-1} = s$. Mnozina G* je s restrikci operace . na G* x G* je grupa, piseme jen G*(.) je grupa.

dk: $(st)(t^{-1}s^{-1}) = s 1 s^{-1} = 1$ a obracene (jenom prohodime zavorky v prvni strane rovnice).  tim jsme dokazali existenci a zaroven podobu a zaroven urcili jednoznacnost (nebot mame poznamku 3.4). Trivialne $1 \in G*$ jje inverzni sam sobe, oeperace je asociativni ze znalosti asociativnosti na G. a tedy G*(.) je grupa.


Terminologie: G*(.) je grupa inertibilnich prvku G.


Priklad 3.5:
1. $M(X)^* (.) = \{\epsilon\}$
2. $T^*(X)=\{f: X \rightarrow X; f \text{ je bijekce}\}$ =: Symetricka grupa na X.. $S(\{1,2,...n\}) =: S_n$.. permutace na n prvcich. $|S_n| = n$
3. $M^*_n(T) = \{A \in M_n(T), A \text{ je regularni matice}\} =: $GL_n(T)(.)$. zobecnena linearni grupa.
4. $Z_n(.)$ je komutativni monid, neni grupa, nebot 0 nema inverzni prvek.
    - $Z^*_n = \{a \in Z_n, NSD(a, n) = 1\}$
    dk: at $a \in Z^*_n$, pak existuje $a^{-1}$ ze $a a^{-1} = 1$ plati v $Z_n(.)$, jinak receno, ze $\exists y \in Z: a . a^{-1} + y . n = 1$ plati v $Z(.)$ TECKA ZDE ZNAMENA NASOBENI V Z!!!
    je-li s $s \in SD(a,n)$, pak $(s | a a^{-1} \wedge s | yn) \Rightarrow s | 1$, tj s = 1.
    Ukazali jsme $Z^*_n \subseteq \{a \in Z_n; NSD(a, n) = 1\}$.
    Naopak necht $a \in Z_n, NSD(a, n) = 1$. z euklidova algroritmu existuji $x, y \in Z$, ze $ax + yn = 1$ tedy $a^{-1} === x mod n$  je inverzni prvek k a v $z_n$.

## 4. Grupy, podgrupy a homomorfismy grup

Definice: at $G(.)$ je grupa, podgrupou grupy $G(.)$ budeme rozumet kazdou podmnozinu H, ze $1 \in H, \forall a,b \in H: ab \in H \wedge a^{-1} \in H$.
- normalni grupa: $\forall g \in G: \forall h \in H: g^{-1} h g \in H$


pozn: je-li G(.) komutativni grupa, pak je kazda jeji podgrupa normalni.

Znaceni: H(.) podgrupa G(.).. $H \leq G$
- H normalni: tto samy ale misto leq trojuhelnik jakoby