```tikz
\usepackage{tikz}
\begin{document}
\begin{tikzpicture}[scale=5]
  % Axes
  \draw[->] (-1.4,0) -- (1.4,0) node[right] {$x$};
  \draw[->] (0,-1.4) -- (0,1.4) node[above] {$y$};

  % Cercle unitaire
  \draw[very thick, blue] (0,0) circle (1);

  % Centre
  \node[below left] at (0,0) {$O$};

  % Angle 0^\circ = 0
  \draw[red] (0,0) -- (1.000,0.000);
  \fill[red] (1.000,0.000) circle (0.02);
  \node[red, anchor=center, fill=white] at (1.30,0.00) {$0$};
  \node[red, anchor=center, fill=white, yshift=-8pt] at (1.30,0.00) {$(1, 0)$};

  % Angle 30^\circ = \frac{\pi}{6}
  \draw[blue!60] (0,0) -- (0.866,0.500);
  \fill[blue!60] (0.866,0.500) circle (0.02);
  \node[blue!60, anchor=south west, fill=white] at (1.13,0.65) {$\frac{\pi}{6}$};
  \node[blue!60, anchor=south west, fill=white, yshift=-8pt] at (1.13,0.65) {$(\frac{\sqrt{3}}{2}, \frac{1}{2})$};

  % Angle 45^\circ = \frac{\pi}{4}
  \draw[green!60!black] (0,0) -- (0.707,0.707);
  \fill[green!60!black] (0.707,0.707) circle (0.02);
  \node[green!60!black, anchor=south west, fill=white] at (0.92,0.92) {$\frac{\pi}{4}$};
  \node[green!60!black, anchor=south west, fill=white, yshift=-8pt] at (0.92,0.92) {$(\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2})$};

  % Angle 60^\circ = \frac{\pi}{3}
  \draw[purple] (0,0) -- (0.500,0.866);
  \fill[purple] (0.500,0.866) circle (0.02);
  \node[purple, anchor=south west, fill=white] at (0.65,1.13) {$\frac{\pi}{3}$};
  \node[purple, anchor=south west, fill=white, yshift=-8pt] at (0.65,1.13) {$(\frac{1}{2}, \frac{\sqrt{3}}{2})$};

  % Angle 90^\circ = \frac{\pi}{2}
  \draw[orange] (0,0) -- (0.000,1.000);
  \fill[orange] (0.000,1.000) circle (0.02);
  \node[orange, anchor=south west, fill=white] at (0.00,1.30) {$\frac{\pi}{2}$};
  \node[orange, anchor=south west, fill=white, yshift=-8pt] at (0.00,1.30) {$(0, 1)$};

  % Angle 120^\circ = \frac{2\pi}{3}
  \draw[brown] (0,0) -- (-0.500,0.866);
  \fill[brown] (-0.500,0.866) circle (0.02);
  \node[brown, anchor=south east, fill=white] at (-0.65,1.13) {$\frac{2\pi}{3}$};
  \node[brown, anchor=south east, fill=white, yshift=-8pt] at (-0.65,1.13) {$(-\frac{1}{2}, \frac{\sqrt{3}}{2})$};

  % Angle 135^\circ = \frac{3\pi}{4}
  \draw[red] (0,0) -- (-0.707,0.707);
  \fill[red] (-0.707,0.707) circle (0.02);
  \node[red, anchor=south east, fill=white] at (-0.92,0.92) {$\frac{3\pi}{4}$};
  \node[red, anchor=south east, fill=white, yshift=-8pt] at (-0.92,0.92) {$(-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2})$};

  % Angle 150^\circ = \frac{5\pi}{6}
  \draw[blue!60] (0,0) -- (-0.866,0.500);
  \fill[blue!60] (-0.866,0.500) circle (0.02);
  \node[blue!60, anchor=south east, fill=white] at (-1.13,0.65) {$\frac{5\pi}{6}$};
  \node[blue!60, anchor=south east, fill=white, yshift=-8pt] at (-1.13,0.65) {$(-\frac{\sqrt{3}}{2}, \frac{1}{2})$};

  % Angle 180^\circ = \pi
  \draw[green!60!black] (0,0) -- (-1.000,0.000);
  \fill[green!60!black] (-1.000,0.000) circle (0.02);
  \node[green!60!black, anchor=south east, fill=white] at (-1.30,0.00) {$\pi$};
  \node[green!60!black, anchor=south east, fill=white, yshift=-8pt] at (-1.30,0.00) {$(-1, 0)$};

  % Angle 210^\circ = \frac{7\pi}{6}
  \draw[purple] (0,0) -- (-0.866,-0.500);
  \fill[purple] (-0.866,-0.500) circle (0.02);
  \node[purple, anchor=north east, fill=white] at (-1.13,-0.65) {$\frac{7\pi}{6}$};
  \node[purple, anchor=north east, fill=white, yshift=-8pt] at (-1.13,-0.65) {$(-\frac{\sqrt{3}}{2}, -\frac{1}{2})$};

  % Angle 225^\circ = \frac{5\pi}{4}
  \draw[orange] (0,0) -- (-0.707,-0.707);
  \fill[orange] (-0.707,-0.707) circle (0.02);
  \node[orange, anchor=north east, fill=white] at (-0.92,-0.92) {$\frac{5\pi}{4}$};
  \node[orange, anchor=north east, fill=white, yshift=-8pt] at (-0.92,-0.92) {$(-\frac{\sqrt{2}}{2}, -\frac{\sqrt{2}}{2})$};

  % Angle 240^\circ = \frac{4\pi}{3}
  \draw[brown] (0,0) -- (-0.500,-0.866);
  \fill[brown] (-0.500,-0.866) circle (0.02);
  \node[brown, anchor=north east, fill=white] at (-0.65,-1.13) {$\frac{4\pi}{3}$};
  \node[brown, anchor=north east, fill=white, yshift=-8pt] at (-0.65,-1.13) {$(-\frac{1}{2}, -\frac{\sqrt{3}}{2})$};

  % Angle 270^\circ = \frac{3\pi}{2}
  \draw[red] (0,0) -- (-0.000,-1.000);
  \fill[red] (-0.000,-1.000) circle (0.02);
  \node[red, anchor=north east, fill=white] at (-0.00,-1.30) {$\frac{3\pi}{2}$};
  \node[red, anchor=north east, fill=white, yshift=-8pt] at (-0.00,-1.30) {$(0, -1)$};

  % Angle 300^\circ = \frac{5\pi}{3}
  \draw[blue!60] (0,0) -- (0.500,-0.866);
  \fill[blue!60] (0.500,-0.866) circle (0.02);
  \node[blue!60, anchor=north west, fill=white] at (0.65,-1.13) {$\frac{5\pi}{3}$};
  \node[blue!60, anchor=north west, fill=white, yshift=-8pt] at (0.65,-1.13) {$(\frac{1}{2}, -\frac{\sqrt{3}}{2})$};

  % Angle 315^\circ = \frac{7\pi}{4}
  \draw[green!60!black] (0,0) -- (0.707,-0.707);
  \fill[green!60!black] (0.707,-0.707) circle (0.02);
  \node[green!60!black, anchor=north west, fill=white] at (0.92,-0.92) {$\frac{7\pi}{4}$};
  \node[green!60!black, anchor=north west, fill=white, yshift=-8pt] at (0.92,-0.92) {$(\frac{\sqrt{2}}{2}, -\frac{\sqrt{2}}{2})$};

  % Angle 330^\circ = \frac{11\pi}{6}
  \draw[purple] (0,0) -- (0.866,-0.500);
  \fill[purple] (0.866,-0.500) circle (0.02);
  \node[purple, anchor=north west, fill=white] at (1.13,-0.65) {$\frac{11\pi}{6}$};
  \node[purple, anchor=north west, fill=white, yshift=-8pt] at (1.13,-0.65) {$(\frac{\sqrt{3}}{2}, -\frac{1}{2})$};

\end{tikzpicture}
\end{document}
```

## 💡 Qu'est-ce que la fonction cosinus ?

### Introduction

La fonction cosinus apparaît naturellement en géométrie lorsque l'on étudie les triangles rectangles. Elle quantifie le rapport entre l'adjacent et l'hypoténuse d'un angle donné. En physique, elle modélise les phénomènes périodiques comme les ondes ou les mouvements oscillatoires. Son étude systématique a conduit aux fonctions trigonométriques fondamentales.

Intuitivement, le cosinus mesure "combien un angle est proche de l'axe horizontal". Plus l'angle est petit, plus le cosinus est proche de 1 (valeur maximale), et plus l'angle s'approche de 90°, plus le cosinus diminue vers 0.

### Définition(s)

> [!abstract] Définition géométrique (triangle rectangle)
> Dans un triangle rectangle, le cosinus d'un angle θ est le rapport entre la longueur du côté adjacent à l'angle et la longueur de l'hypoténuse.
>
> $$\cos(\theta) = \frac{\text{adjacent}}{\text{hypoténuse}}$$
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
>   \node[red] at (0.8,0.15) {$\theta$};
>
>   % Labels
>   \node[below] at (1.5,0) {adjacent};
>   \node[right] at (3,1) {oppose};
>   \node[above left] at (1.5,1.2) {hypotenuse};
>
>   % Formule
>   \node[below] at (1.5,-0.5) {$\cos(\theta) = \frac{adjacent}{hypoténuse}$};
> \end{tikzpicture}
> \end{document}
> ```

> [!abstract] Définition analytique (cercle trigonométrique)
> Sur le cercle trigonométrique de rayon 1, le cosinus d'un angle θ est l'abscisse du point M correspondant à cet angle.
>
> $$\cos(\theta) = x_M$$
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

Ces deux définitions sont équivalentes car le cercle trigonométrique n'est qu'une généralisation du triangle rectangle où l'hypoténuse a toujours longueur 1.

---

## 🔍 Comment ça fonctionne ?

### L'idée centrale

Le cosinus est une fonction périodique de période 2π, ce qui signifie qu'elle se répète tous les 360°. Elle est paire (symétrique par rapport à l'axe des ordonnées), ce qui reflète la symétrie des angles dans le cercle trigonométrique.

**Exemple concret:** Si on mesure l'ombre d'un bâton vertical à midi, sa longueur est proportionnelle au cosinus de l'angle du soleil. Plus le soleil est haut, plus l'ombre est courte (cosinus proche de 0), et inversement.

### Domaine et contraintes

Le cosinus est défini pour tous les nombres réels, car on peut toujours tracer un angle correspondant sur le cercle trigonométrique. Cependant, sa valeur est toujours comprise entre -1 et 1, car le cercle a un rayon de 1.

En dehors de cet intervalle, le cosinus n'est pas défini car il n'existe pas de point sur le cercle trigonométrique qui aurait une abscisse supérieure à 1 ou inférieure à -1.

---

## 📊 Propriétés principales

### Parité

Le cosinus est une fonction paire, ce qui signifie que cos(-θ) = cos(θ). Cela vient du fait que les angles opposés ont la même projection sur l'axe horizontal.

$$\cos(-\theta) = \cos(\theta)$$

**Pourquoi ?** La symétrie du cercle trigonométrique fait que les angles θ et -θ ont la même abscisse.

**Conséquence pratique:** Cela simplifie les calculs avec des angles négatifs.

### Périodicité

Le cosinus est périodique de période 2π, ce qui signifie que cos(θ + 2π) = cos(θ). Cela reflète le fait que le cercle trigonométrique se répète tous les 360°.

$$\cos(\theta + 2\pi) = \cos(\theta)$$

**Pourquoi ?** Ajouter 2π à un angle revient à faire un tour complet du cercle, donc on revient au même point.

**Conséquence pratique:** On peut réduire tout angle modulo 2π pour simplifier les calculs.

### Valeurs remarquables

| Angle (rad) | Angle (deg) | cos(θ) | Pourquoi c'est intéressant |
|---|---|---|---|
| 0 | 0° | 1 | Valeur maximale, cosinus de l'angle nul |
| π/2 | 90° | 0 | Transition entre positif et négatif |
| π | 180° | -1 | Valeur minimale, cosinus de l'angle droit |
| 3π/2 | 270° | 0 | Retour à zéro avant la fin du cycle |

---

## 🎯 Applications et exemples

### Exemple 1: Calcul de la hauteur d'un bâtiment

**Contexte:** Un géomètre veut mesurer la hauteur d'un bâtiment en utilisant un bâton vertical et son ombre.

**Problème:** Le bâton fait 1.5m et son ombre mesure 2m. L'ombre du bâtiment mesure 50m. Quelle est la hauteur du bâtiment?

**Résolution:**

Étape 1: On a deux triangles semblables (même angles)
$$\frac{\text{hauteur du bâton}}{\text{ombre du bâton}} = \frac{\text{hauteur du bâtiment}}{\text{ombre du bâtiment}}$$

Étape 2: On connaît cos(θ) = adjacent/hypoténuse = ombre du bâton / longueur du bâton
$$\cos(\theta) = \frac{2}{1.5 + \sqrt{5}}$$

Étape 3: On calcule la hauteur du bâtiment
$$\text{hauteur} = 50 \times \frac{1.5}{\sqrt{5}}$$

Résultat final:
$$\text{hauteur} = 30 \sqrt{2} \approx 42.43 \text{m}$$

**Interprétation:** Le cosinus permet de relier les dimensions d'objets inaccessibles à partir de mesures simples.

---

### Exemple 2: Analyse de signal

**Contexte:** En traitement du signal, le cosinus est utilisé pour décomposer les signaux en fréquences.

**Problème:** Un signal est donné par f(t) = 3cos(2πt) + 2cos(4πt). Quelle est sa fréquence fondamentale?

**Résolution:**

Étape 1: Identifier les composantes cosinus
$$f(t) = 3\cos(2\pi t) + 2\cos(4\pi t)$$

Étape 2: Calculer les fréquences
$$\text{Fréquence} = \frac{\omega}{2\pi} = \frac{2\pi}{2\pi} = 1 \text{Hz pour la première composante}$$
$$\text{Fréquence} = \frac{4\pi}{2\pi} = 2 \text{Hz pour la deuxième composante}$$

Résultat final:
$$\text{Fréquence fondamentale} = 1 \text{Hz}$$

**Interprétation:** Le cosinus permet d'analyser les composantes fréquentielles d'un signal.

---

## 🔗 Liens avec d'autres concepts

- **[[Fonction sinus]]**: Le cosinus est la dérivée du sinus, et inversement. Ils sont liés par la relation fondamentale sin²θ + cos²θ = 1.
- **[[Fonction exponentielle]]**: La fonction exponentielle complexe e^(iθ) = cosθ + i sinθ relie les fonctions trigonométriques aux nombres complexes.
- **[[Séries de Fourier]]**: Le cosinus est une des fonctions de base utilisées pour décomposer des signaux périodiques en séries de Fourier.

---

## 📝 À retenir

> [!summary] L'essentiel
>
> Le cosinus mesure la projection d'un angle sur l'axe horizontal, soit dans un triangle rectangle, soit sur le cercle trigonométrique. C'est une fonction périodique et paire, toujours comprise entre -1 et 1. Elle est fondamentale en géométrie, physique et analyse des signaux.
>
> Formules clés:
> - cos(θ) = adjacent/hypoténuse (triangle rectangle)
> - cos(θ + 2π) = cos(θ) (périodicité)
> - cos(-θ) = cos(θ) (parité)
>
> Ce qu'il faut retenir: Le cosinus capture l'idée de "projection horizontale" d'un angle, ce qui le rend utile pour modéliser des phénomènes oscillatoires et périodiques.

#Fonction/trigonometrique #{analyse} #{geometrie}