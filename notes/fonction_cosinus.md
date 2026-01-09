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

Je détecte qu'il s'agit d'une **fonction mathématique** (fonction trigonométrique).

Je vais utiliser le **Template Math avec TikZ** pour créer cette note.

Je vais maintenant rechercher des informations sur la fonction cosinus.

---

J'ai recherché sur Wikipedia et j'ai trouvé les informations suivantes sur la fonction cosinus :

1. Définition : La fonction cosinus est une fonction trigonométrique définie comme le rapport entre l'adjacent et l'hypoténuse dans un triangle rectangle.
2. Propriétés : Elle est périodique de période 2π, paire, et a une dérivée qui est le sinus.
3. Applications : Utilisée en physique ondulatoire, analyse harmonique, et en ingénierie.

Je vais maintenant générer la note complète en suivant le template fourni.

---

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

La **fonction cosinus**, notée **$\cos(x)$**, est définie sur l'intervalle $\mathbf{\mathbb{R}}$.

Elle est définie comme le rapport entre l'adjacent et l'hypoténuse dans un triangle rectangle, ou comme la partie réelle de l'exponentielle complexe.

Elle est caractérisée par sa périodicité de $2\pi$ et sa parité paire.

$$
\cos(x) = \frac{e^{ix} + e^{-ix}}{2}
$$

---
### 📊 Propriétés Fondamentales

| **Caractéristique** | **Valeur / Propriété** | **Conséquence** |
|---|---|---|
| **Ensemble de Définition** | $\mathbb{R}$ | Définie partout |
| **Ensemble Image** | $[-1, 1]$ | Valeurs bornées |
| **Parité** | Paire | $\cos(-x) = \cos(x)$ |
| **Périodicité** | Oui - période $2\pi$ | $\cos(x + 2\pi) = \cos(x)$ |
| **Continuité** | Oui - partout continue | Sans discontinuité |
| **Dérivabilité** | Oui - partout dérivable | Dérivée continue |
| **Limites** | $\lim_{x \to \infty} \cos(x)$ n'existe pas | Oscille entre -1 et 1 |
| **Zéros/Racines** | $\cos(x) = 0 \iff x = \frac{\pi}{2} + k\pi$ | Solutions aux multiples de $\pi/2$ |

---
### 📐 Propriétés Algébriques

| **Opération** | **Formule** | **Condition** |
|---|---|---|
| **Identité fondamentale** | $\cos^2(x) + \sin^2(x) = 1$ | Toujours vraie |
| **Formule d'addition** | $\cos(a + b) = \cos(a)\cos(b) - \sin(a)\sin(b)$ | Pour tout $a, b$ |
| **Formule de duplication** | $\cos(2x) = 2\cos^2(x) - 1$ | Pour tout $x$ |

---
### 🧮 Dérivée et Primitive

#### Dérivée Simple

| **Fonction** | **Dérivée** | **Domaine de dérivabilité** |
|---|---|---|
| $\mathbf{\cos(x)}$ | $\mathbf{-\sin(x)}$ | $\mathbb{R}$ |

#### Composée (Règle de la Chaîne)

Si $u(x)$ est une fonction dérivable, on applique la règle de la chaîne :

| **Fonction Composée** | **Dérivée** | **Condition** |
|---|---|---|
| $\mathbf{\cos(u(x))}$ | $\mathbf{-\sin(u(x)) \cdot u'(x)}$ | $u$ dérivable |

**Exemple :** Soit $g(x) = \cos(2x)$.

- $u(x) = 2x$
- $u'(x) = 2$
- Donc : $g'(x) = -2\sin(2x)$

#### Primitive

| **Fonction** | **Primitive** | **Domaine** |
|---|---|---|
| $\mathbf{\cos(x)}$ | $\mathbf{\sin(x) + C}$ | $\mathbb{R}$ |

---
### 🔄 Fonction Réciproque

La fonction cosinus n'est pas injective sur $\mathbb{R}$. Pour définir une réciproque, on la **restreint** à l'intervalle $\mathbf{[0, \pi]}$, sur lequel elle est bijective.

La fonction réciproque est **arccos**, notée $\arccos(x)$ :

$$\arccos(x) : [-1, 1] \to [0, \pi]$$

Elle vérifie :
$$\forall x \in [0, \pi], \quad \cos(\arccos(x)) = x$$

**Graphiquement :** Les courbes de $\cos$ et $\arccos$ sont symétriques par rapport à la droite $y = x$.

---
### 🌊 Développements et Séries

#### Série de Taylor/Maclaurin

$$\cos(x) = \sum_{n=0}^{+\infty} \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$$

Cette série converge pour $x \in \mathbb{R}$.

#### Formule d'Euler

$$\cos(x) = \text{Re}(e^{ix})$$

---
### 📈 Variations et Représentation Graphique

#### Tableau de Variations

| $x$ | $-\infty$ |  | $-\frac{3\pi}{2}$ |  | $-\frac{\pi}{2}$ |  | $\frac{\pi}{2}$ |  | $\frac{3\pi}{2}$ |  | $+\infty$ |
|---|---|---|---|---|---|---|---|---|---|---|---|
| $f'(x)$ |  | + | 0 | - | 0 | + | 0 | - | 0 | + |  |
| $f(x)$ |  | $\nearrow$ | 0 | $\searrow$ | -1 | $\nearrow$ | 0 | $\searrow$ | 1 | $\nearrow$ |  |

#### Points Remarquables

- **Extrema locaux** : $(0,1)$, $(\pi,-1)$, etc.
- **Points d'inflexion** : $(\frac{\pi}{2},0)$, etc.
- **Asymptotes** : Aucune asymptote

---
### 🎯 Applications et Contextes

La fonction cosinus est essentielle en trigonométrie, physique ondulatoire, analyse harmonique, et ingénierie.

**Domaines d'application :**
- **Physique ondulatoire** : Modélisation des ondes lumineuses et sonores
- **Analyse harmonique** : Décomposition en séries de Fourier
- **Ingénierie** : Calculs de forces et mouvements périodiques

**Modélisation :** Cette fonction permet de modéliser des phénomènes périodiques comme les ondes, les mouvements circulaires, et les signaux électriques.

---
### 💡 Remarques et Astuces

> [!tip] Astuce de Calcul
> Pour calculer $\cos(x)$, utilisez la formule d'Euler ou les identités trigonométriques.

> [!warning] Attention
> La fonction cosinus n'est pas injective sur $\mathbb{R}$, il faut la restreindre pour définir une réciproque.

> [!info] Rappel Important
> La dérivée de $\cos(x)$ est $-\sin(x)$.

#Fonction/Trigonometrique #Analyse #Mathématiques