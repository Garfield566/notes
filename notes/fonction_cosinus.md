```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}

\begin{document}
\begin{tikzpicture}
\begin{axis}[
    axis lines=middle,
    grid=both,
    domain=-6.28:6.28,
    samples=200,
    xlabel={$x$},
    ylabel={$f(x)$},
    width=10cm,
    height=8cm
]
\addplot[blue, thick] {cos(deg(x))};
\end{axis}
\end{tikzpicture}
\end{document}
```

## 💡 Qu'est-ce que la fonction cosinus ?

### Introduction

La fonction cosinus apparaît naturellement en trigonométrie pour résoudre des problèmes géométriques liés aux triangles rectangles. Elle quantifie la proportion entre l'adjacent et l'hypoténuse dans un triangle rectangle, mais son importance dépasse largement ce cadre initial. En physique, elle décrit les oscillations périodiques comme les mouvements des pendules ou les ondes lumineuses. Son étude a conduit à des avancées majeures en analyse, notamment dans la compréhension des séries de Fourier et des équations différentielles.

### Définition(s)

> [!abstract] Définition géométrique (triangle rectangle)
> Dans un triangle rectangle, le cosinus d'un angle θ est le rapport entre la longueur du côté adjacent à l'angle et la longueur de l'hypoténuse.
>
> $$
> \cos(\theta) = \frac{\text{adjacent}}{\text{hypoténuse}}
> $$

> [!abstract] Définition analytique (fonction circulaire)
> La fonction cosinus est définie comme la coordonnée x d'un point M sur le cercle unité (rayon 1) dont l'angle polaire est θ.
>
> $$
> \cos(\theta) = x \quad \text{où} \quad M = (x, y) \text{ sur le cercle unité}
> $$

Ces deux définitions sont équivalentes car le cercle unité peut être vu comme un triangle rectangle dont l'hypoténuse est de longueur 1.

---

## 🔍 Comment ça fonctionne ?

### L'idée centrale

Le cosinus mesure comment un angle "compresse" une longueur. Plus l'angle θ augmente, plus la composante horizontale (cosinus) diminue, reflétant la transition progressive d'une orientation horizontale à verticale. Cette propriété est cruciale pour modéliser les phénomènes oscillatoires où les amplitudes varient périodiquement.

### Domaine et contraintes

La fonction cosinus est définie pour tous les angles réels, mais elle est périodique de période 2π, ce qui signifie qu'elle se répète tous les 360° :

$$
\cos(\theta + 2\pi) = \cos(\theta)
$$

Cette périodicité vient du fait que le cercle trigonométrique est fermé : après un tour complet, on revient au point de départ.

---

## 📊 Propriétés principales

### Symétrie et parité

Le cosinus est une fonction paire, ce qui signifie qu'elle est symétrique par rapport à l'axe des ordonnées :

$$
\cos(-\theta) = \cos(\theta)
$$

**Pourquoi ?** Cela vient du fait que l'angle -θ correspond à l'angle θ mesuré dans le sens inverse, mais la projection sur l'axe x reste la même.

**Conséquence pratique:** Cette symétrie simplifie le calcul des intégrales et permet de réduire les calculs à des angles positifs.

### Valeurs remarquables

| Angle (rad) | Angle (deg) | Valeur | Signification |
|------------|------------|--------|--------------|
| 0          | 0°         | 1      | Maximum de la fonction |
| π/2        | 90°        | 0      | Transition entre positif et négatif |
| π          | 180°       | -1     | Minimum de la fonction |
| 3π/2       | 270°       | 0      | Retour à zéro |

---

## 🎯 Applications et exemples

### Exemple 1: Calcul de la hauteur d'un bâtiment

**Contexte:** Un ingénieur doit calculer la hauteur d'un bâtiment en utilisant un théodolite qui mesure un angle de 30° avec le sol.

**Résolution:**

1. L'ingénieur mesure la distance horizontale entre le théodolite et le bâtiment: 50 mètres.
2. La hauteur h du bâtiment est donnée par:
   $$
   \tan(30°) = \frac{h}{50} \implies h = 50 \times \tan(30°)
   $$
3. Sachant que $\tan(30°) = \frac{\sin(30°)}{\cos(30°)} = \frac{1/2}{\sqrt{3}/2} = \frac{1}{\sqrt{3}}$
4. Donc:
   $$
   h = 50 \times \frac{1}{\sqrt{3}} \approx 28.87 \text{ mètres}
   $$

**Interprétation:** Le cosinus permet ici de relier une mesure angulaire à une distance verticale, ce qui est essentiel en topographie et en ingénierie.

---

### Exemple 2: Oscillation d'un pendule

**Contexte:** Un pendule de longueur L oscille avec une amplitude θ.

**Résolution:**

1. La position horizontale x(t) du pendule est donnée par:
   $$
   x(t) = L \cos(\omega t)
   $$
   où ω est la fréquence angulaire.
2. Pour un pendule simple, ω = √(g/L) où g est l'accélération gravitationnelle.
3. Si L = 1 m et θ₀ = 10° (0.1745 rad), alors:
   $$
   x(t) = \cos(\sqrt{9.81} \times t)
   $$

**Interprétation:** Le cosinus modélise parfaitement le mouvement périodique du pendule, montrant comment sa position varie dans le temps.

---

## 🔗 Liens avec d'autres concepts

- **[[Fonction sinus]]**: Le cosinus et le sinus sont liés par la relation fondamentale $\sin^2(\theta) + \cos^2(\theta) = 1$, qui vient directement du théorème de Pythagore appliqué au cercle unité.
- **[[Séries de Fourier]]**: Le cosinus est une des fonctions de base utilisées pour décomposer des signaux périodiques en composantes fréquentielles.
- **[[Fonctions exponentielles]]**: L'identité d'Euler $e^{i\theta} = \cos(\theta) + i\sin(\theta)$ relie le cosinus aux nombres complexes et aux exponentielles.

---

## 📝 À retenir

> [!summary] L'essentiel
>
> La fonction cosinus mesure la projection d'un angle sur l'axe horizontal. Elle est périodique, paire et atteint ses valeurs extrêmes à 0, π/2, π et 3π/2. Ses applications vont de la géométrie aux oscillations mécaniques en passant par l'analyse des signaux. La relation fondamentale avec le sinus et l'exponentielle complexe en fait un outil central en mathématiques.
>
> Formule clé:
> $$
> \cos(\theta) = \frac{e^{i\theta} + e^{-i\theta}}{2}
> $$

#Fonction/Trigonométrie #Analyse #Oscillations