```tikz
\usepackage{tikz}
\begin{document}
\begin{tikzpicture}[scale=1.5]
  % Triangle
  \draw[very thick] (0,0) -- (5,0) -- (3.20,2.40) -- cycle;

  % Points
  \fill (0,0) circle (0.05);
  \fill (5,0) circle (0.05);
  \fill (3.20,2.40) circle (0.05);

  % Labels des sommets
  \node[below left] at (0,0) {$A$};
  \node[below right] at (5,0) {$B$};
  \node[above] at (3.20,2.40) {$C$};

  % Labels des côtés
  \node[below] at (2.5,0) {$c = 5$};
  \node[left] at (1.60,1.20) {$b = 4$};
  \node[right] at (4.10,1.20) {$a = 3$};

  % Arc d'angle en A
  \fill[blue!40] (0,0) -- (0.90,0.00) arc (0.0:36.9:0.9) -- cycle;
  \node at (0.47,0.16) {$37^\circ$};

  % Arc d'angle en B
  \fill[yellow!60] (5,0) -- (4.46,0.72) arc (126.9:180.0:0.9) -- cycle;
  \node at (4.55,0.22) {$53^\circ$};

  % Arc d'angle en C
  \fill[green!40] (3.20,2.40) -- (2.48,1.86) arc (-143.1:-53.1:0.9) -- cycle;
  \node at (3.13,1.91) {$90^\circ$};
\end{tikzpicture}
\end{document}
```

## 💡 Qu'est-ce que le théorème de Pythagore ?

### Introduction

Le théorème de Pythagore est l'un des résultats les plus fondamentaux de la géométrie euclidienne. Il apparaît naturellement dans l'étude des triangles rectangles, où il relie les longueurs des côtés de manière surprenante. Son nom vient du mathématicien grec Pythagore, bien que des traces de sa connaissance remontent à des civilisations antérieures comme les Babyloniens.

Ce théorème est à la base de nombreuses applications pratiques, de la construction d'édifices à la navigation, en passant par la physique. Son élégance réside dans la relation simple qu'il établit entre les trois côtés d'un triangle rectangle.

### Définition(s)

> [!abstract] Définition géométrique
> Dans un triangle rectangle, le carré de l'hypoténuse (le côté opposé à l'angle droit) est égal à la somme des carrés des deux autres côtés.
>
> $$\text{Si } ABC \text{ est un triangle rectangle en } A, \text{ alors } AB^2 + AC^2 = BC^2$$
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
>   % Labels
>   \node[below] at (1.5,0) {$AB$};
>   \node[right] at (3,1) {$AC$};
>   \node[above left] at (1.5,1.2) {$BC$};
>
>   % Carrés sur les côtés
>   \draw[dashed, blue] (0,0) rectangle (3,0.5);
>   \draw[dashed, green] (3,0) rectangle (3.5,2);
>   \draw[dashed, red] (0,0) rectangle (0.5,2.5);
>
>   % Formules
>   \node[blue] at (1.5,0.25) {$AB^2$};
>   \node[green] at (3.25,1) {$AC^2$};
>   \node[red] at (0.25,1.25) {$BC^2$};
> \end{tikzpicture}
> \end{document}
> ```

> [!abstract] Définition algébrique
> Pour tout triangle rectangle, la relation entre les côtés peut s'exprimer par l'équation:
>
> $$a^2 + b^2 = c^2$$
>
> où $a$ et $b$ sont les longueurs des côtés adjacents à l'angle droit, et $c$ est la longueur de l'hypoténuse.
>
> **Illustration graphique (SI POSSIBLE):**
> ```tikz
> \begin{document}
> \begin{tikzpicture}[scale=2]
>   % Triangle rectangle
>   \draw[very thick] (0,0) -- (3,0) -- (3,2) -- cycle;
>
>   % Labels
>   \node[below] at (1.5,0) {$a$};
>   \node[right] at (3,1) {$b$};
>   \node[above left] at (1.5,1.2) {$c$};
>
>   % Angle droit
>   \draw (3,0) -- (2.8,0) -- (2.8,0.2) -- (3,0.2);
> \end{tikzpicture}
> \end{document}
> ```

Ces deux définitions sont équivalentes : la première est visuelle et géométrique, tandis que la seconde est algébrique et plus abstraite. La première permet de comprendre intuitivement pourquoi la relation est vraie, tandis que la seconde permet de l'utiliser dans des calculs.

---

## 🔍 Comment ça fonctionne ?

### L'idée centrale

Le théorème de Pythagore exprime une relation fondamentale entre les côtés d'un triangle rectangle. L'intuition géométrique vient du fait que les aires des carrés construits sur les côtés adjacents à l'angle droit s'additionnent pour donner l'aire du carré construit sur l'hypoténuse.

Prenons un exemple simple : un triangle rectangle avec des côtés de 3 et 4. Selon le théorème, l'hypoténuse doit être $\sqrt{3^2 + 4^2} = 5$. Cela forme un triangle dit "3-4-5", qui est un exemple classique.

### Domaine et contraintes

Le théorème s'applique strictement aux triangles rectangles, c'est-à-dire aux triangles qui ont un angle de 90 degrés. Si le triangle n'est pas rectangle, la relation ne tient plus. Cependant, il existe des généralisations comme le théorème de Pythagore généralisé pour les triangles non rectangles.

---

## 📊 Propriétés principales

### Relation fondamentale

Le théorème établit une relation entre les trois côtés d'un triangle rectangle.

$$a^2 + b^2 = c^2$$

**Pourquoi ?** Cette relation vient du fait que les aires des carrés construits sur les côtés adjacents à l'angle droit s'additionnent pour donner l'aire du carré construit sur l'hypoténuse. C'est une conséquence directe de la géométrie des triangles rectangles.

**Conséquence pratique:** Cette propriété permet de calculer la longueur d'un côté d'un triangle rectangle si on connaît les deux autres. C'est une application fondamentale en géométrie, en physique et en ingénierie.

---

### Réciproque du théorème

Si dans un triangle, le carré d'un côté est égal à la somme des carrés des deux autres côtés, alors ce triangle est rectangle.

$$a^2 + b^2 = c^2 \implies \text{triangle rectangle en } C$$

**Pourquoi ?** La réciproque est vraie car la relation $a^2 + b^2 = c^2$ est une condition nécessaire et suffisante pour qu'un triangle soit rectangle. Cela permet de prouver qu'un triangle est rectangle sans avoir à mesurer ses angles.

---

### Généralisation aux dimensions supérieures

En dimension 3, le théorème de Pythagore s'étend aux triangles rectangles dans l'espace. Pour un triangle rectangle dans un plan, la relation reste la même. Cependant, pour un triangle rectangle dans l'espace, la relation devient plus complexe.

---

## 🧮 Calculs et manipulations

### Calcul de l'hypoténuse

Dans un triangle rectangle, si on connaît les deux côtés adjacents à l'angle droit, on peut calculer l'hypoténuse.

$$c = \sqrt{a^2 + b^2}$$

**Pourquoi cette formule?** Cette formule vient directement du théorème de Pythagore. Elle permet de calculer la longueur de l'hypoténuse à partir des deux autres côtés.

### Calcul d'un côté adjacent

Si on connaît l'hypoténuse et un côté adjacent, on peut calculer l'autre côté adjacent.

$$a = \sqrt{c^2 - b^2}$$

**Pourquoi cette formule?** Cette formule est une réarrangement du théorème de Pythagore. Elle permet de calculer un côté adjacent à partir de l'hypoténuse et de l'autre côté adjacent.

### Cas particuliers remarquables

| Triangle | Côtés | Hypoténuse | Pourquoi c'est intéressant |
|---|---|---|---|
| 3-4-5 | 3, 4 | 5 | Triangle rectangle classique, souvent utilisé pour vérifier l'équerrage |
| 5-12-13 | 5, 12 | 13 | Autre exemple classique de triangle rectangle |
| 8-15-17 | 8, 15 | 17 | Exemple moins connu mais toujours valide |

---

## 🎯 Applications et exemples

### Exemple 1: Calcul de la diagonale d'un rectangle

**Contexte:** Dans un rectangle de dimensions 3 et 4, on veut calculer la longueur de la diagonale.

**Résolution:**

Étape 1: On considère le rectangle comme un triangle rectangle en divisant la diagonale.
$$\text{Diagonale} = \sqrt{3^2 + 4^2}$$

Étape 2: On calcule les carrés des côtés.
$$3^2 = 9$$
$$4^2 = 16$$

Étape 3: On additionne les carrés.
$$9 + 16 = 25$$

Étape 4: On prend la racine carrée.
$$\sqrt{25} = 5$$

Résultat final:
$$\text{Diagonale} = 5$$

**Interprétation:** La diagonale d'un rectangle de dimensions 3 et 4 est de 5. Cela montre que le théorème de Pythagore peut être utilisé pour calculer des distances dans des figures géométriques.

---

### Exemple 2: Vérification d'un angle droit

**Contexte:** On veut vérifier si un angle est droit en mesurant les côtés.

**Résolution:**

Étape 1: On mesure les trois côtés du triangle.
$$a = 6$$
$$b = 8$$
$$c = 10$$

Étape 2: On calcule les carrés des côtés.
$$6^2 = 36$$
$$8^2 = 64$$
$$10^2 = 100$$

Étape 3: On vérifie la relation.
$$36 + 64 = 100$$

Résultat final:
$$36 + 64 = 100$$

**Interprétation:** La relation est vérifiée, donc l'angle est droit. Cela montre que le théorème de Pythagore peut être utilisé pour vérifier la nature d'un angle.

---

## 🔗 Liens avec d'autres concepts

- **[[Théorème de Thalès]]**: Le théorème de Thalès est souvent utilisé en conjonction avec le théorème de Pythagore pour résoudre des problèmes de géométrie.
- **[[Trigonométrie]]**: Les fonctions trigonométriques comme le sinus et le cosinus sont directement liées au théorème de Pythagore dans le cercle trigonométrique.
- **[[Vecteurs]]**: Le théorème de Pythagore est utilisé pour calculer la norme d'un vecteur dans un espace euclidien.

---

## 📝 À retenir

> [!summary] L'essentiel
>
> Le théorème de Pythagore est une relation fondamentale entre les côtés d'un triangle rectangle. Il s'exprime par la formule $a^2 + b^2 = c^2$, où $a$ et $b$ sont les côtés adjacents à l'angle droit, et $c$ est l'hypoténuse.
>
> Ce théorème permet de calculer la longueur d'un côté d'un triangle rectangle si on connaît les deux autres. Il a de nombreuses applications pratiques, de la construction à la navigation, en passant par la physique.
>
> La réciproque du théorème permet de vérifier si un triangle est rectangle en utilisant uniquement les longueurs des côtés. Le théorème de Pythagore est également lié à d'autres concepts mathématiques comme le théorème de Thalès, la trigonométrie et les vecteurs.

#Théorème/{géométrie} #Pythagore #triangle_rectangle