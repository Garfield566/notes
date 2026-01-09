Voici une fiche complète pour la fonction sinus, basée sur votre modèle :

---

# Fonction Sinus

La **fonction sinus**, notée **$\sin(x)$**, est définie sur l'intervalle $\mathbf{\mathbb{R}}$.

Fonction trigonométrique fondamentale, elle représente le rapport entre l'ordonnée d'un point et la longueur du rayon dans le cercle unité.

Elle est caractérisée par sa périodicité et son comportement oscillatoire.

$$ \sin(x) = \text{ordonnée du point sur le cercle unité d'angle } x \text{ (en radians)} $$

---

### 📊 Propriétés Fondamentales

| **Caractéristique** | **Valeur / Propriété** | **Conséquence** |
|---|---|---|
| **Ensemble de Définition** | $\mathbb{R}$ | Définie partout |
| **Ensemble Image** | $[-1, 1]$ | Valeurs bornées |
| **Parité** | Impaire | $\sin(-x) = -\sin(x)$ |
| **Périodicité** | Oui - période $2\pi$ | $\sin(x + 2\pi) = \sin(x)$ |
| **Continuité** | Oui partout | Fonction continue |
| **Dérivabilité** | Oui partout | Fonction dérivable |
| **Limites** | $\lim_{x \to \pm\infty} \sin(x) = \text{oscille entre } -1 \text{ et } 1$ | Pas de limite finie |
| **Zéros/Racines** | $\sin(x) = 0 \iff x = k\pi, k \in \mathbb{Z}$ | Zéros aux multiples de $\pi$ |

---

### 📐 Propriétés Algébriques

| **Opération** | **Formule** | **Condition** |
|---|---|---|
| **Formule d'addition** | $\sin(a+b) = \sin a \cos b + \cos a \sin b$ | $a, b \in \mathbb{R}$ |
| **Formule de duplication** | $\sin(2x) = 2 \sin x \cos x$ | $x \in \mathbb{R}$ |
| **Formule de Moivre** | $\sin^n(x) = \frac{1}{2^{n-1}} \sum_{k=0}^{\lfloor (n-1)/2 \rfloor} (-1)^k \binom{n}{2k+1} \cos^{n-2k-1}(x)$ | $n \in \mathbb{N}$ |

---

### 🧮 Dérivée et Primitive

#### Dérivée Simple

| **Fonction** | **Dérivée** | **Domaine de dérivabilité** |
|---|---|---|
| $\sin(x)$ | $\cos(x)$ | $\mathbb{R}$ |

#### Composée (Règle de la Chaîne)

Si $u(x)$ est dérivable, alors :

| **Fonction Composée** | **Dérivée** | **Condition** |
|---|---|---|
| $\sin(u(x))$ | $\cos(u(x)) \cdot u'(x)$ | $u$ dérivable |

**Exemple :** Soit $g(x) = \sin(x^2)$.

- $u(x) = x^2$
- $u'(x) = 2x$
- Donc : $g'(x) = 2x \cos(x^2)$

#### Primitive

| **Fonction** | **Primitive** | **Domaine** |
|---|---|---|
| $\sin(x)$ | $-\cos(x) + C$ | $\mathbb{R}$ |

---

### 🔄 Fonction Réciproque

La fonction sinus est **non injective** sur $\mathbb{R}$.

Pour définir une réciproque, on la **restreint** à l'intervalle $\mathbf{[-\frac{\pi}{2}, \frac{\pi}{2}]}$, sur lequel elle est bijective.

La fonction réciproque est **l'arc sinus**, notée $\arcsin$ :

$$ \arcsin : [-1, 1] \to \left[-\frac{\pi}{2}, \frac{\pi}{2}\right] $$

Elle vérifie :
$$ \forall x \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right], \quad \sin(\arcsin(x)) = x $$

**Graphiquement :** Les courbes de $\sin$ et $\arcsin$ sont symétriques par rapport à la droite $y = x$.

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

| $x$ | $-\frac{\pi}{2}$ |  | $\frac{\pi}{2}$ |  | $\frac{3\pi}{2}$ |  | $2\pi$ |
|---|---|---|---|---|---|---|---|
| $\sin'(x) = \cos(x)$ | 0 | + | 0 | - | 0 | + | 0 |
| $\sin(x)$ | -1 | $\nearrow$ | 1 | $\searrow$ | -1 | $\nearrow$ | 1 |

#### Points Remarquables

- **Extrema locaux** : $(k\pi + \frac{\pi}{2}, (-1)^k)$
- **Points d'inflexion** : $(k\pi, 0)$
- **Asymptotes** : Aucune

---

### 🎯 Applications et Contextes

La fonction sinus est omniprésente en physique, ingénierie et mathématiques.

**Domaines d'application :**
- **Physique** : Modélisation des ondes (lumière, son)
- **Ingénierie** : Analyse des circuits électriques (AC)
- **Mathématiques** : Résolution d'équations différentielles

**Modélisation :** Cette fonction permet de modéliser tout phénomène périodique.

---

### 💡 Remarques et Astuces

> [!tip] Astuce de Calcul
> Pour calculer $\sin(x)$ pour des angles non standards, utilisez les identités trigonométriques ou les séries de Taylor.

> [!warning] Attention
> La fonction sinus est périodique : ne pas oublier de considérer tous les angles possibles !

> [!info] Rappel Important
> $\sin(0) = 0$, $\sin(\frac{\pi}{2}) = 1$, $\sin(\pi) = 0$, $\sin(\frac{3\pi}{2}) = -1$

---

#Fonction/Trigonométrique #Analyse #Périodique