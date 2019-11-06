**Definice** $g\inG$, G grupa. **Rad prvku g** je $|<g>_G|$, znacime: $ord_G(G)$

**Poznamka 5.4**: Rad prvku $g \in G$, G grupa, je nemensi takove $n \in \mathbb{N}$, ze $g^n = 1$. Pokud existuje, jinak $\infty$. Navic, je-li konecny, pak deli libovolny exponent prvku g.

*Dukaz*: At existuje $k\in \mathbb{N}: g^k = 1$. At $n \in \mathbb{Z}$ libovolne, oznacime $q = n \div k, r = n \mod k \rightarrow g^n = g^{qk + r} = (g^k)^q g^r = g^r$, tj $<g>_G = \{g^r; r \in \mathbb{Z}\}$. Pro $k$ minimalni mozne  pak dostavame $\forall i, j, 0 \leq i \leq j: g^i \neq g^j \text{jinak by} g^{i-j} = 1 \rightarrow \text{spor}$. tj. $ord_G(g) = k$. Je-li $n \in \mathbb{N}$ libovolny exponent prvku g, pak $1=g^n=g^r \rightarrow r = 0 \rightarrow k | n$

**Veta 5.5**: Bud $G(\cdot$ cyklicka grupa.

1) je-li G nekonecna, pak $G(\cdot) \equiv \mathbb{Z}(+)$
2) Je-li $\mathbb{N} \in n = |G| \rightarrow G(\cdot) \equiv \mathbb{Z}_n(+)$

*dk*:

1) Z pozor 5.2 (cviceni)... ex. homomorfismus $\phi \in \mathbb{Z} \rightarrow G, \text{kde} <g>_G = G$. Dle 5.4 je $Ker(\phi)=\{0\}$, tj. $\phi$ je proste, zaroven $n \rightarrow g^n$, $\phi$ je zrejme na, tj. $phi$ je izomorfismus grup.
2) At $\phi: \mathbb{Z}_n \rightarrow G$ je definovano vztahem $\phi(k) = g^k$, kde je g nejaky querator? grupy G., overize ze $\phi$ je homomorfismus.
    $x, y \in \mathbb{Z}_n... \phi((x+y)\mod n) = \phi(x) \phi(y) = g^x g^y$. $g^{(x+y)\mod n} = g^{(x+y)\mod n} \cdot g^{(x+y)\mod n}  = g^{x+y} = g^x g^y$
    Navic $\phi$ je na, dle 5.4 a teddy je i prosta, jelikoz $|\mathbb{Z}_n| = |G| < \infty$.

**Dusledek 5.6**: podgrpy cyklickych grup jsou opet cyklicke.

*dukaz*: Dle 5.5 to staci ukazat pro $G = \mathbb{Z}(+)$ a $G = \mathbb{Z}_n(+)$ (kde n je pr cislo).
Vime, ze podgruoy grupy $\mathbb{Z}(+)$ jsou prave tvaru $n \mathbb{Z} = <n>_\mathbb{Z}$, kde n je pr cislo nebo nula. Tedy vsechny jsu cyklicke.

Dale uvazujeme $F_n: \mathbb{Z} \rightarrow \mathbb{Z}_n$ grupovy kover. Je-li $H \leq \mathbb{Z}_n$, pak $F_n^{1} \leq \mathbb{Z}$ a pote je i $H = F_n(F_n^{-1}(H))$ cyklicka.

## Eulerova veta a kryptologicke aplikace

**Poznamka 6.1 (podgrupy $Z_n$ podrobneji)**: At $k,n \in \mathbb{N}, k > 1, k | n. \rightarrow <\frac{n}{k}>_{\mathbb{Z}_n(+)}$ je jedina podgrupa grupy $Z_n(+)$ radu k. Navic pro kazde $a \in \mathbb{Z} \smallsetminus \{0\}: <a> = <\frac{n}{k}> \Leftrightarrow NSD(a, n) = \frac{n}{k}$ .

*Dukaz*: At $h | n, h < n$, pak  $\{0, h, 2h, ... (\frac{n}{h} - 1)d\} \leq \mathbb{Z}_n$ podgrupa radu $\frac{n}{h}$.
Tj ukazali jsme existenci podgrupy radu k. At navic $a \in \mathbb{Z}_n \smallsetminus \{0\}, h := NSD(a,n)$. Ukazeme, ze $<a>= <h>$. Jelikoz $h | a, a \in <h> \rightarrow <a> \subseteq <h>$. Z Bezontovy rovosti dostaneme $x,y \in \mathbb{Z}, h = xa + yn \Rightarrow h = (xa) \mod n \Rightarrow d \in <a> \rightarrow <h> \subseteq <a>$. Dusledek 5.6 $\Rightarrow$ kazda podgrupa $\mathbb{Z}_n(+)$ je tvaru $<a>$, kde $a \in \mathbb{Z}_n$.

**Definujeme**: Eulerovou funkci nazyvame zobrazeni $\phi \mathbb{N} \rightarrow \mathbb{N}$ kde $\phi(n) := |\mathbb{Z}_n^*(\cdot)| = |\{a \in \mathbb{Z}_n; NSD(a,n) = 1\}|$ pro $n > 1, \phi(1) := 1$.

**Veta 6.2**: Necht $p_1 < p_2 < ... <p_k$ prvocisla, $r_1,...r_k \in \mathbb{N}$ Pak $\phi(\prod\limits_{i=1}^k p_i^{r_i}) = \prod\limits_{i=1}^k (p_i-1)p_i^{r_i-1} = )$.

*Dukaz*: Nejprve at $k=1, p_1 = p, r_1 = r$. Potom pocet soudelnych 