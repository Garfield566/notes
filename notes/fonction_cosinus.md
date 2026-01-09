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

[GRAPHIQUE TIKZ SERA INSÉRÉ ICI]
## 💡 Définition et Caractérisation

La **fonction cosinus**, notée **$\cos(x)$**, est définie sur l'intervalle $\mathbf{\mathbb{R}}$ (ensemble des nombres réels).

Le cosinus d'un angle est défini comme le rapport entre la longueur de l'adjacent et l'hypoténuse dans un triangle rectangle. En analyse, il s'agit d'une fonction périodique, continue et dérivable sur $\mathbb{R}$.

Elle est caractérisée par sa périodicité de $2\pi$ et sa symétrie paire.

$$ \cos(x) = \frac{e^{ix} + e^{-ix}}{2} $$

---
### 📊 Propriétés Fondamentales

| **Caractéristique** | **Valeur / Propriété** | **Conséquence** |
|---|---|---|
| **Ensemble de Définition** | $\mathbb{R}$ | La fonction est définie pour tout nombre réel |
| **Ensemble Image** | $[-1, 1]$ | Le cosinus prend ses valeurs entre -1 et 1 |
| **Parité** | Paire | $\cos(-x) = \cos(x)$ |
| **Périodicité** | Oui - période $2\pi$ | $\cos(x + 2\pi) = \cos(x)$ |
| **Continuité** | Oui - partout continue | La fonction n'a pas de discontinuité |
| **Dérivabilité** | Oui - partout dérivable | La dérivée est $-\sin(x)$ |
| **Limites** | $\lim_{x \to \infty} \cos(x)$ n'existe pas | La fonction oscille entre -1 et 1 |
| **Zéros/Racines** | $\cos(x) = 0 \iff x = \frac{\pi}{2} + k\pi, k \in \mathbb{Z}$ | Les zéros sont aux multiples de $\frac{\pi}{2}$ |

---
### 📐 Propriétés Algébriques

| **Opération** | **Formule** | **Condition** |
|---|---|---|
| **Formule d'addition** | $\cos(a + b) = \cos(a)\cos(b) - \sin(a)\sin(b)$ | $a, b \in \mathbb{R}$ |
| **Formule de soustraction** | $\cos(a - b) = \cos(a)\cos(b) + \sin(a)\sin(b)$ | $a, b \in \mathbb{R}$ |
| **Formule de duplication** | $\cos(2x) = 2\cos^2(x) - 1$ | $x \in \mathbb{R}$ |

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

**Exemple :** Soit $g(x) = \cos(3x^2)$.

- $u(x) = 3x^2$
- $u'(x) = 6x$
- Donc : $g'(x) = -\sin(3x^2) \cdot 6x = -6x \sin(3x^2)$

#### Primitive

| **Fonction** | **Primitive** | **Domaine** |
|---|---|---|
| $\mathbf{\cos(x)}$ | $\mathbf{\sin(x) + C}$ | $\mathbb{R}$ |

---
### 🔄 Fonction Réciproque

La fonction cosinus n'est pas injective sur $\mathbb{R}$. Pour définir une réciproque, on la restreint à l'intervalle $\mathbf{[0, \pi]}$, sur lequel elle est bijective.

La fonction réciproque est **l'arccosinus**, notée $\arccos(x)$ :

$$ \arccos(x) : [-1, 1] \to [0, \pi] $$

Elle vérifie :
$$ \forall x \in [-1, 1], \quad \cos(\arccos(x)) = x $$

**Graphiquement :** Les courbes de $\cos$ et $\arccos$ sont symétriques par rapport à la droite $y = x$.

---
### 🌊 Développements et Séries

#### Série de Taylor/Maclaurin

$$ \cos(x) = \sum_{n=0}^{+\infty} \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \dots $$

Cette série converge pour $x \in \mathbb{R}$.

#### Formule d'Euler

$$ \cos(x) = \frac{e^{ix} + e^{-ix}}{2} $$

---
### 📈 Variations et Représentation Graphique

#### Tableau de Variations

| $x$ | $-\infty$ |  | $-\frac{3\pi}{2}$ |  | $-\frac{\pi}{2}$ |  | $\frac{\pi}{2}$ |  | $\frac{3\pi}{2}$ |  | $+\infty$ |
|---|---|---|---|---|---|---|---|---|---|---|---|
| $\cos'(x)$ |  | + |  | - |  | + |  | - |  | + |  |
| $\cos(x)$ |  | $\nearrow$ | 0 | $\searrow$ | -1 | $\nearrow$ | 0 | $\searrow$ | 1 | $\nearrow$ | 0 |

#### Points Remarquables

- **Extrema locaux** : Maximums en $x = 2k\pi$, minimums en $x = (2k+1)\pi$
- **Points d'inflexion** : Aux zéros de $\cos(x)$
- **Asymptotes** : Aucune asymptote

---
### 🎯 Applications et Contextes

Le cosinus est omniprésent en mathématiques et en physique :

**Domaines d'application :**
- **Trigonométrie** : Calculs dans les triangles
- **Physique ondulatoire** : Modélisation des ondes
- **Analyse harmonique** : Décomposition en séries de Fourier
- **Informatique graphique** : Calculs de rotations

**Modélisation :** Le cosinus permet de modéliser des phénomènes périodiques comme les ondes sonores, les mouvements oscillatoires, et les variations saisonnières.

---
### 💡 Remarques et Astuces

> [!tip] Astuce de Calcul
> Pour calculer $\cos(x)$ pour un angle en degrés, utilisez la conversion $x_{rad} = x_{deg} \times \frac{\pi}{180}$.

> [!warning] Attention
> Ne confondez pas $\cos(x)$ avec $\cosh(x)$ (cosinus hyperbolique).

> [!info] Rappel Important
> La dérivée de $\cos(x)$ est $-\sin(x)$, et sa primitive est $\sin(x) + C$.

#Fonction/Trigonométrique #Analyse #Mathématiques