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
\addplot[blue, thick] {sin(deg(x))};
\end{axis}
\end{tikzpicture}
\end{document}
```

## 💡 Qu'est-ce que la fonction sinus ?

### Introduction

La fonction sinus apparaît naturellement en géométrie lorsque l'on étudie les triangles rectangles. Elle permet de relier les angles aux longueurs des côtés, ce qui est crucial pour résoudre des problèmes de mesure et de construction. En physique, elle modélise les phénomènes périodiques comme les ondes sonores ou les mouvements oscillatoires.

Intuitivement, le sinus d'un angle dans un triangle rectangle représente la proportion entre la longueur du côté opposé à cet angle et la longueur de l'hypotenuse. C'est une mesure de "l'élévation" relative par rapport à l'angle.

### Définition(s)

> [!abstract] Définition géométrique (triangle rectangle)
> Dans un triangle rectangle ABC avec angle droit en C, le sinus d'un angle α est le rapport entre la longueur du côté opposé (BC) et la longueur de l'hypotenuse (AB).
>
> $$\sin(\alpha) = \frac{\text{opposé}}{\text{hypotenuse}} = \frac{BC}{AB}$$
>
> **Illustration graphique (SI POSSIBLE):**
> ```tikz
> \begin{document}
> \begin{tikzpicture}[scale=2]
>   % Triangle rectangle
>   \draw[very thick] (0,0) -- (3,0) -- (3,2) -- cycle;
>
>   % Angle droit
>   \draw (3,0) -- (2.8,0) -- (2.8,0.2) -- (3,0.2);
>
>   % Arc pour l'angle (en rouge)
>   \draw[very thick, red] (0.6,0) arc (0:33.7:0.6);
>   \node[red] at (0.8,0.15) {$\alpha$};
>
>   % Labels
>   \node[below] at (1.5,0) {adjacent};
>   \node[right] at (3,1) {opposé};
>   \node[above left] at (1.5,1.2) {hypotenuse};
>
>   % Formule
>   \node[below] at (1.5,-0.5) {$\sin(\alpha) = \frac{\text{opposé}}{\text{hypotenuse}}$};
> \end{tikzpicture}
> \end{document}
> ```

> [!abstract] Définition analytique (cercle trigonométrique)
> Sur le cercle trigonométrique de rayon 1, le sinus d'un angle θ est l'ordonnée du point M correspondant à cet angle.
>
> $$\sin(\theta) = y$$
>
> **Illustration graphique (SI POSSIBLE):**
> ```tikz
> \begin{document}
> \begin{tikzpicture}[scale=3]
>   % Axes
>   \draw[->] (-1.3,0) -- (1.3,0) node[right] {$x$};
>   \draw[->] (0,-1.3) -- (0,1.3) node[above] {$y$};
>
>   % Cercle
>   \draw[thick] (0,0) circle (1);
>
>   % Angle (exemple: 40 degrés)
>   \draw[very thick, red] (0.5,0) arc (0:40:0.5);
>   \node[red] at (0.6,0.2) {$\theta$};
>
>   % Point sur le cercle
>   \draw[thick, blue] (0,0) -- (0.766,0.643);
>   \fill[blue] (0.766,0.643) circle (0.03);
>   \node[blue, above right] at (0.766,0.643) {$M$};
>
>   % Projection pour cos (ligne verticale rouge)
>   \draw[very thick, red, dashed] (0.766,0) -- (0.766,0.643);
>
>   % Projection pour cos (ligne horizontale verte)
>   \draw[very thick, green!60!black] (0,0) -- (0.766,0);
>   \node[green!60!black, below] at (0.383,0) {$\cos(\theta)$};
>
>   % Projection pour sin
>   \draw[thick, orange] (0,0) -- (0,0.643);
>   \node[orange, left] at (0,0.32) {$\sin(\theta)$};
>
>   % Graduations
>   \node[below left] at (0,0) {$O$};
>   \node[below] at (1,0) {$1$};
>   \node[left] at (0,1) {$1$};
> \end{tikzpicture}
> \end{document}
> ```

Ces deux définitions sont équivalentes car le cercle trigonométrique est une généralisation du triangle rectangle où l'hypotenuse est toujours de longueur 1.

---

## 🔍 Comment ça fonctionne ?

### L'idée centrale

La fonction sinus est une fonction périodique qui oscille entre -1 et 1. Elle modélise parfaitement les phénomènes qui se répètent régulièrement comme les ondes, les mouvements pendulaires ou les variations saisonnières.

Prenons un exemple simple: si on considère un point tournant autour d'un cercle à vitesse constante, sa position verticale (ordonnée) suit exactement une fonction sinus par rapport à l'angle parcouru.

### Domaine et contraintes

La fonction sinus est définie pour tous les nombres réels, c'est-à-dire sur l'ensemble ℝ. Cela vient du fait que l'on peut définir un angle pour n'importe quel nombre réel en utilisant la notion d'angle orienté.

Cependant, pour des angles supérieurs à 2π (360°), la fonction sinus se répète, ce qui est la manifestation mathématique de sa périodicité.

---

## 📊 Propriétés principales

### Périodicité

La fonction sinus se répète tous les 2π radians (360°). C'est pourquoi on dit qu'elle est périodique de période 2π.

$$\sin(\theta + 2\pi) = \sin(\theta)$$

**Pourquoi ?** Parce que faire un tour complet autour du cercle trigonométrique ramène au même point de départ.

**Conséquence pratique:** On peut réduire n'importe quel angle modulo 2π pour simplifier les calculs.

### Symétrie

La fonction sinus est impaire, ce qui signifie qu'elle est symétrique par rapport à l'origine.

$$\sin(-\theta) = -\sin(\theta)$$

**Pourquoi ?** Sur le cercle trigonométrique, un angle négatif correspond à un angle positif dans le sens inverse, ce qui inverse la position verticale.

### Valeurs remarquables

| Angle (radians) | Angle (degrés) | Valeur du sinus | Pourquoi c'est intéressant |
|-----------------|----------------|-----------------|-----------------------------|
| 0               | 0°             | 0               | Point de départ sur l'axe horizontal |
| π/6             | 30°            | 1/2             | Triangle équilatéral divisé |
| π/4             | 45°            | √2/2            | Angle bissecteur du carré |
| π/2             | 90°            | 1               | Point le plus haut du cercle |
| π               | 180°           | 0               | Retour sur l'axe horizontal |
| 3π/2            | 270°           | -1              | Point le plus bas du cercle |

---

## 🎯 Applications et exemples

### Exemple 1: Calcul de la hauteur d'un arbre

**Contexte:** Un arbre de 10 mètres de haut fait un angle de 30° avec le sol. Quelle est la hauteur réelle de l'arbre?

**Résolution:**

Étape 1: On modélise la situation avec un triangle rectangle où l'hypotenuse est la longueur de l'arbre (10m) et l'angle adjacent est de 30°.

Étape 2: On utilise la définition du sinus:
$$\sin(30°) = \frac{\text{hauteur réelle}}{\text{longueur de l'arbre}}$$

Étape 3: On connaît sin(30°) = 0.5, donc:
$$0.5 = \frac{h}{10} \implies h = 5m$$

**Interprétation:** La hauteur réelle de l'arbre est de 5 mètres. Cet exemple montre comment le sinus permet de calculer des distances inaccessibles directement.

---

### Exemple 2: Modélisation d'une onde sonore

**Contexte:** Une onde sonore peut être modélisée par une fonction sinus. Si on a une onde de fréquence 440 Hz, quelle est sa période?

**Résolution:**

Étape 1: La fréquence est de 440 Hz, ce qui signifie 440 oscillations par seconde.

Étape 2: La période T est l'inverse de la fréquence:
$$T = \frac{1}{f} = \frac{1}{440} \approx 0.00227s$$

Étape 3: L'onde peut donc être modélisée par:
$$y(t) = A \cdot \sin(2\pi \cdot 440 \cdot t + \phi)$$

**Interprétation:** Cette modélisation permet de comprendre comment les ondes sonores se propagent et comment elles sont perçues par l'oreille humaine.

---

## 🔗 Liens avec d'autres concepts

- **[[Fonction cosinus]]**: Le sinus et le cosinus sont liés par une relation fondamentale: $\sin^2(\theta) + \cos^2(\theta) = 1$. Ils représentent respectivement l'ordonnée et l'abscisse d'un point sur le cercle trigonométrique.
- **[[Fonction tangente]]**: La tangente est définie comme le rapport entre le sinus et le cosinus: $\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)}$.
- **[[Séries de Fourier]]**: Le sinus est une des fonctions de base utilisées dans les séries de Fourier pour décomposer des signaux périodiques complexes.

---

## 📝 À retenir

> [!summary] L'essentiel
>
> La fonction sinus est une fonction périodique qui modélise les phénomènes oscillatoires. Elle est définie géométriquement comme le rapport entre l'opposé et l'hypotenuse dans un triangle rectangle, ou comme l'ordonnée d'un point sur le cercle trigonométrique.
>
> Ses propriétés principales sont sa périodicité (période 2π), son caractère impair (sin(-x) = -sin(x)), et ses valeurs remarquables aux angles standards.
>
> Elle trouve des applications dans de nombreux domaines: calcul de distances inaccessibles, modélisation d'ondes, analyse de signaux, etc.

#Fonction/trigonometrique #analyse #geometrie