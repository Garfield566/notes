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

```tikz
\begin{document}
\begin{tikzpicture}[scale=3]
  % Axes
  \draw[->] (-1.3,0) -- (1.3,0) node[right] {$x$};
  \draw[->] (0,-1.3) -- (0,1.3) node[above] {$y$};

  % Cercle
  \draw[thick] (0,0) circle (1);

  % Angle (exemple: 40 degrés)
  \draw[very thick, red] (0.5,0) arc (0:40:0.5);
  \node[red] at (0.6,0.2) {$\theta$};

  % Point sur le cercle
  \draw[thick, blue] (0,0) -- (0.766,0.643);
  \fill[blue] (0.766,0.643) circle (0.03);
  \node[blue, above right] at (0.766,0.643) {$M$};

  % Projection pour cos (ligne verticale rouge)
  \draw[very thick, red, dashed] (0.766,0) -- (0.766,0.643);

  % Projection pour cos (ligne horizontale verte)
  \draw[very thick, green!60!black] (0,0) -- (0.766,0);
  \node[green!60!black, below] at (0.383,0) {$\cos(\theta)$};

  % Projection pour sin
  \draw[thick, orange] (0,0) -- (0,0.643);
  \node[orange, left] at (0,0.32) {$\sin(\theta)$};

  % Graduations
  \node[below left] at (0,0) {$O$};
  \node[below] at (1,0) {$1$};
  \node[left] at (0,1) {$1$};
\end{tikzpicture}
\end{document}
```

## 💡 Définition et Caractérisation

La **fonction sinus**, notée **$\sin(x)$**, est définie sur l'intervalle $\mathbf{\mathbb{R}}$ (ensemble des nombres réels).

Elle est caractérisée par sa périodicité de $2\pi$ et sa nature impaire. La fonction sinus est une fonction trigonométrique fondamentale qui associe à un angle $\theta$ la coordonnée verticale du point correspondant sur le cercle unité.

$$ \sin(x) = \text{coordonnée verticale du point sur le cercle unité d'angle } x $$

Cette fonction est essentielle en trigonométrie, en physique des ondes, et en analyse mathématique.

---
### 📊 Propriétés Fondamentales

| **Caractéristique** | **Valeur / Propriété** | **Conséquence** |
|---|---|---|
| **Ensemble de Définition** | $\mathbb{R}$ | La fonction est définie pour tout nombre réel |
| **Ensemble Image** | $[-1, 1]$ | La fonction est bornée entre -1 et 1 |
| **Parité** | Impaire | $\sin(-x) = -\sin(x)$ |
| **Périodicité** | $2\pi$ | $\sin(x + 2\pi) = \sin(x)$ |
| **Continuité** | Continue partout | La fonction est continue sur $\mathbb{R}$ |
| **Dérivabilité** | Dérivable partout | La dérivée est $\cos(x)$ |
| **Limites** | $\lim_{x \to \pm\infty} \sin(x)$ n'existe pas | La fonction oscille entre -1 et 1 |
| **Zéros/Racines** | $\sin(x) = 0 \iff x = k\pi, k \in \mathbb{Z}$ | Les zéros sont les multiples de $\pi$ |

---
### 📐 Propriétés Algébriques

| **Opération** | **Formule** | **Condition** |
|---|---|---|
| **Addition** | $\sin(a + b) = \sin(a)\cos(b) + \cos(a)\sin(b)$ | $a, b \in \mathbb{R}$ |
| **Soustraction** | $\sin(a - b) = \sin(a)\cos(b) - \cos(a)\sin(b)$ | $a, b \in \mathbb{R}$ |
| **Double Angle** | $\sin(2x) = 2\sin(x)\cos(x)$ | $x \in \mathbb{R}$ |

---
### 🧮 Dérivée et Primitive

#### Dérivée Simple

| **Fonction** | **Dérivée** | **Domaine de dérivabilité** |
|---|---|---|
| $\mathbf{\sin(x)}$ | $\mathbf{\cos(x)}$ | $\mathbb{R}$ |

#### Composée (Règle de la Chaîne)

Si $u(x)$ est une fonction dérivable, on applique la règle de la chaîne :

| **Fonction Composée** | **Dérivée** | **Condition** |
|---|---|---|
| $\mathbf{\sin(u(x))}$ | $\mathbf{\cos(u(x)) \cdot u'(x)}$ | $u(x) \in \mathbb{R}$ |

**Exemple :** Soit $g(x) = \sin(3x^2)$.

- $u(x) = 3x^2$
- $u'(x) = 6x$
- Donc : $g'(x) = \cos(3x^2) \cdot 6x = 6x\cos(3x^2)$

#### Primitive

| **Fonction** | **Primitive** | **Domaine** |
|---|---|---|
| $\mathbf{\sin(x)}$ | $\mathbf{-\cos(x) + C}$ | $\mathbb{R}$ |

---
### 🔄 Fonction Réciproque

La fonction sinus est **non injective** sur $\mathbb{R}$. Pour définir une réciproque, on la **restreint** à l'intervalle $\mathbf{[-\frac{\pi}{2}, \frac{\pi}{2}]}$, sur lequel elle est bijective.

La fonction réciproque est **arcsin**, notée $\arcsin(x)$ :

$$ \arcsin(x) : [-1, 1] \to \left[-\frac{\pi}{2}, \frac{\pi}{2}\right] $$

Elle vérifie :
$$ \forall x \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right], \quad \sin(\arcsin(x)) = x $$

**Graphiquement :** Les courbes de $\sin(x)$ et $\arcsin(x)$ sont symétriques par rapport à la droite $y = x$.

---
### 🌊 Développements et Séries

#### Série de Taylor/Maclaurin

$$ \sin(x) = \sum_{n=0}^{+\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{6} + \frac{x^5}{120} - \dots $$

Cette série converge pour $x \in \mathbb{R}$.

#### Formule d'Euler

$$ \sin(x) = \frac{e^{ix} - e^{-ix}}{2i} $$

---
### 📈 Variations et Représentation Graphique

#### Tableau de Variations

| $x$ | $-\infty$ |  | $-\frac{3\pi}{2}$ |  | $-\frac{\pi}{2}$ |  | $\frac{\pi}{2}$ |  | $\frac{3\pi}{2}$ |  | $+\infty$ |
|---|---|---|---|---|---|---|---|---|---|---|---|
| $\sin'(x)$ |  | + |  | - |  | + |  | - |  | + |  |
| $\sin(x)$ |  | $\nearrow$ | 1 | $\searrow$ | -1 | $\nearrow$ | 1 | $\searrow$ | -1 | $\nearrow$ |  |

#### Points Remarquables

- **Extrema locaux** : $(k\pi + \frac{\pi}{2}, (-1)^k)$ pour $k \in \mathbb{Z}$
- **Points d'inflexion** : $(k\pi, 0)$ pour $k \in \mathbb{Z}$
- **Asymptotes** : Aucune asymptote

---
### 🎯 Applications et Contextes

La fonction sinus est omniprésente en mathématiques et en sciences. Elle permet de modéliser des phénomènes périodiques comme les ondes sonores, les ondes lumineuses, et les mouvements oscillatoires.

**Domaines d'application :**
- **Trigonométrie** : Résolution de triangles, calculs d'angles.
- **Physique ondulatoire** : Description des ondes sinusoïdales.
- **Signal périodique** : Analyse des signaux électriques et acoustiques.
- **Mécanique** : Étude des mouvements circulaires et harmoniques.

**Modélisation :** La fonction sinus permet de modéliser des phénomènes comme les vibrations d'une corde de guitare, les ondes électromagnétiques, et les mouvements des pendules.

---
### 💡 Remarques et Astuces

> [!tip] Astuce de Calcul
> Pour calculer $\sin(x)$ pour un angle non standard, utilisez les identités trigonométriques comme $\sin^2(x) + \cos^2(x) = 1$.

> [!warning] Attention
> La fonction sinus n'est pas injective sur $\mathbb{R}$, il faut donc la restreindre pour définir une réciproque.

> [!info] Rappel Important
> La dérivée de $\sin(x)$ est $\cos(x)$, et sa primitive est $-\cos(x) + C$.

#Fonction/Trigonométrique #Trigonométrie #Périodicité