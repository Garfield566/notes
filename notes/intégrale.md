## 💡 Qu'est-ce que l'intégrale ?

### Introduction

L'intégrale est née d'un besoin fondamental en mathématiques et en physique : calculer des quantités accumulées. Imaginez que vous voulez calculer la distance parcourue par un objet en mouvement dont la vitesse change constamment. Ou encore, la surface sous une courbe représentant des données économiques. L'intégrale répond à ces questions en permettant de "somme" des infiniment petits.

À l'origine, les mathématiciens comme Archimède utilisaient des méthodes géométriques pour calculer des aires. Newton et Leibniz ont ensuite formalisé le concept d'intégrale comme l'inverse de la dérivée, créant ainsi le calcul infinitésimal.

### Définition(s)

> [!abstract] Définition (intuitive)
> L'intégrale d'une fonction sur un intervalle est la somme des aires (algébriques) sous sa courbe entre deux points. C'est une généralisation du calcul de l'aire d'un rectangle à des formes infiniment complexes.

> [!abstract] Définition (mathématique)
> Soit \( f \) une fonction continue sur \([a, b]\). L'intégrale de \( f \) de \( a \) à \( b \) est définie par:
>
> $$\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^n f(x_i^*) \Delta x_i$$
>
> où \( \Delta x_i = x_i - x_{i-1} \) et \( x_i^* \) est un point dans \([x_{i-1}, x_i]\).

**Illustration graphique (SI POSSIBLE):**
```tikz
\begin{document}
\begin{tikzpicture}[scale=1.5]
  \draw[->] (-0.5,0) -- (3.5,0) node[right] {$x$};
  \draw[->] (0,-0.5) -- (0,2.5) node[above] {$f(x)$};
  \draw[domain=0:3, smooth, variable=\x, blue] plot ({\x}, {0.5*\x*\x});
  \draw[red, dashed] (0,0) -- (3,4.5);
  \draw[red, dashed] (3,0) -- (3,4.5);
  \fill[blue!20] (0,0) -- plot[domain=0:3, smooth, variable=\x] ({\x}, {0.5*\x*\x}) -- (3,0) -- cycle;
  \node at (1.5,3.5) {$\int_a^b f(x) \, dx$};
\end{tikzpicture}
\end{document}
```

> [!abstract] Définition (via la dérivée)
> L'intégrale est aussi définie comme l'inverse de la dérivée. Si \( F \) est une primitive de \( f \), alors:
>
> $$\int_a^b f(x) \, dx = F(b) - F(a)$$

Expliquez comment ces définitions se relient et pourquoi elles sont équivalentes.

---

## 🔍 Comment ça fonctionne ?

### L'idée centrale

L'intégrale permet de calculer l'aire sous une courbe en la décomposant en une infinité de rectangles infiniment fins. Plus la fonction est complexe, plus cette décomposition est nécessaire pour obtenir une approximation précise.

Par exemple, si vous avez une courbe représentant la vitesse d'un véhicule en fonction du temps, l'intégrale de cette courbe entre deux instants vous donnera la distance parcourue pendant cette période.

### Domaine et contraintes

L'intégrale est définie pour les fonctions continues sur un intervalle fermé \([a, b]\). Si la fonction a des discontinuités, l'intégrale peut encore exister si les discontinuités sont "maîtrisées" (par exemple, un nombre fini de discontinuités de première espèce).

En dehors de cet intervalle, l'intégrale n'est pas définie. Pour les fonctions non continues, il faut souvent utiliser des intégrales impropres ou des intégrales au sens de Cauchy.

---

## 📊 Propriétés principales

### Linéarité de l'intégrale

L'intégrale est linéaire, ce qui signifie que:
$$\int_a^b (kf(x) + lg(x)) \, dx = k \int_a^b f(x) \, dx + l \int_a^b g(x) \, dx$$

**Pourquoi ?** Cette propriété vient du fait que l'intégrale est une somme infinie, et les sommes infinies respectent la linéarité.

**Conséquence pratique:** Cela permet de décomposer les intégrales complexes en intégrales plus simples.

### Intégrale d'une fonction paire ou impaire

Pour une fonction paire \( f(-x) = f(x) \):
$$\int_{-a}^a f(x) \, dx = 2 \int_0^a f(x) \, dx$$

Pour une fonction impaire \( f(-x) = -f(x) \):
$$\int_{-a}^a f(x) \, dx = 0$$

**Pourquoi ?** Les symétries de la fonction se reflètent dans l'intégrale.

**Conséquence pratique:** Cela simplifie grandement le calcul des intégrales de fonctions symétriques.

### Intégrale et dérivée

L'intégrale est l'inverse de la dérivée. Si \( F \) est une primitive de \( f \), alors:
$$\int_a^b f(x) \, dx = F(b) - F(a)$$

**Pourquoi ?** C'est le théorème fondamental du calcul infinitésimal.

**Conséquence pratique:** Cela permet de calculer des intégrales en utilisant des primitives.

---

## 🧮 Calculs et manipulations

### Calcul de l'intégrale d'une fonction polynomiale

Pour calculer l'intégrale d'une fonction polynomiale \( P(x) = a_nx^n + \dots + a_0 \), on utilise la formule:
$$\int P(x) \, dx = \frac{a_n}{n+1}x^{n+1} + \dots + a_0x + C$$

**Pourquoi cette formule?** Chaque terme \( x^k \) est intégré en \( \frac{x^{k+1}}{k+1} \).

**Cas particuliers:**
- Pour \( k = 0 \), \( \int a_0 \, dx = a_0x + C \)
- Pour \( k = 1 \), \( \int a_1x \, dx = \frac{a_1}{2}x^2 + C \)

| Fonction | Intégrale | Pourquoi c'est intéressant |
|---|---|---|
| \( x \) | \( \frac{x^2}{2} + C \) | Base pour intégrer des polynômes |
| \( x^2 \) | \( \frac{x^3}{3} + C \) | Utilisé en physique pour l'énergie cinétique |
| \( 1 \) | \( x + C \) | Intégrale la plus simple |

---

## 🎯 Applications et exemples

### Exemple 1: Calcul de l'aire sous une parabole

**Contexte:** On veut calculer l'aire sous la parabole \( f(x) = x^2 \) entre \( x = 0 \) et \( x = 1 \).

**Résolution:**

Étape 1: Trouver la primitive de \( f(x) \)
$$\int x^2 \, dx = \frac{x^3}{3} + C$$

Étape 2: Appliquer le théorème fondamental
$$\int_0^1 x^2 \, dx = \left. \frac{x^3}{3} \right|_0^1 = \frac{1}{3} - 0 = \frac{1}{3}$$

Résultat final:
$$\frac{1}{3}$$

**Interprétation:** L'aire sous la parabole entre 0 et 1 est \( \frac{1}{3} \). Cela montre que l'intégrale permet de calculer des aires même pour des formes courbes.

---

### Exemple 2: Calcul de la distance parcourue

**Contexte:** Un objet se déplace avec une vitesse \( v(t) = 3t^2 \) m/s. Quelle distance parcourt-il entre \( t = 0 \) et \( t = 2 \) secondes?

**Résolution:**

Étape 1: Intégrer la vitesse
$$\int_0^2 3t^2 \, dt = \left. t^3 \right|_0^2 = 8 - 0 = 8$$

Résultat final:
$$8 \text{ mètres}$$

**Interprétation:** L'objet parcourt 8 mètres en 2 secondes. Cela montre comment l'intégrale permet de passer de la vitesse à la distance.

---

## 🔗 Liens avec d'autres concepts

- **[[Dérivée]]**: L'intégrale est l'inverse de la dérivée, comme le montre le théorème fondamental du calcul.
- **[[Série de Taylor]]**: Les intégrales sont utilisées pour calculer les coefficients des séries de Taylor.
- **[[Équations différentielles]]**: Les intégrales permettent de résoudre des équations différentielles.

---

## 📝 À retenir

> [!summary] L'essentiel
>
> L'intégrale est un outil fondamental pour calculer des quantités accumulées, comme des aires, des distances ou des travaux. Elle est définie comme la limite d'une somme de rectangles infiniment fins sous une courbe. Les propriétés clés incluent la linéarité, les symétries et le lien avec la dérivée. Les intégrales sont utilisées pour calculer des aires, des volumes, des centres de masse, et résoudre des équations différentielles.
>
> Formule clé:
> $$\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^n f(x_i^*) \Delta x_i$$
>
> Ce qu'il faut retenir:
> - L'intégrale est l'inverse de la dérivée.
> - Elle permet de calculer des aires sous des courbes.
> - Elle est utilisée en physique pour calculer des quantités comme la distance ou le travail.

#Fonction/{intégrale} #Calcul_infinitésimal #Analyse