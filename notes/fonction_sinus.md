Voici un exemple concret de fiche fonction en utilisant la fonction exponentielle comme modèle. Vous pouvez adapter ce template pour d'autres fonctions en remplissant les sections correspondantes.

---

## 💡 Définition et Caractérisation

La **fonction exponentielle**, notée **$e^x$**, est définie sur l'intervalle $\mathbf{\mathbb{R}}$.

[DESCRIPTION DÉTAILLÉE DE LA FONCTION]
La fonction exponentielle est la fonction qui, à tout réel $x$, associe $e^x$ où $e$ est la base des logarithmes naturels (environ 2,71828).

Elle est caractérisée par [PROPRIÉTÉ CARACTÉRISTIQUE PRINCIPALE].
La fonction exponentielle est la seule fonction continue qui est égale à sa dérivée et qui vaut 1 en 0.

$$[FORMULE DÉFINITION PRINCIPALE]$$
$e^x = \sum_{n=0}^{+\infty} \frac{x^n}{n!}$ (développement en série)

---

### 📊 Propriétés Fondamentales

| **Caractéristique** | **Valeur / Propriété** | **Conséquence** |
|---|---|---|
| **Ensemble de Définition** | $\mathbb{R}$ | La fonction est définie pour tout réel. |
| **Ensemble Image** | $]0, +\infty[$ | La fonction exponentielle est toujours positive. |
| **Parité** | Ni paire ni impaire | $e^{-x} = \frac{1}{e^x}$ |
| **Périodicité** | Non périodique | La fonction croît indéfiniment. |
| **Continuité** | Continue sur $\mathbb{R}$ | La fonction est continue partout. |
| **Dérivabilité** | Dérivable sur $\mathbb{R}$ | $e' = e$ |
| **Limites** | $\lim_{x \to -\infty} e^x = 0$ et $\lim_{x \to +\infty} e^x = +\infty$ | La fonction tend vers 0 à gauche et vers l'infini à droite. |
| **Zéros/Racines** | $e^x = 0 \iff x = -\infty$ | La fonction n'a pas de racine réelle. |

---

### 📐 Propriétés Algébriques

| **Opération** | **Formule** | **Condition** |
|---|---|---|
| **Produit** | $e^{a+b} = e^a \cdot e^b$ | $a, b \in \mathbb{R}$ |
| **Puissance** | $e^{a \cdot b} = (e^a)^b$ | $a, b \in \mathbb{R}$ |
| **Inverse** | $e^{-a} = \frac{1}{e^a}$ | $a \in \mathbb{R}$ |

---

### 🧮 Dérivée et Primitive

#### Dérivée Simple

| **Fonction** | **Dérivée** | **Domaine de dérivabilité** |
|---|---|---|
| $\mathbf{e^x}$ | $\mathbf{e^x}$ | $\mathbb{R}$ |

#### Composée (Règle de la Chaîne)

Si $u(x)$ est une fonction dérivable [CONDITIONS SUR u], on applique la règle de la chaîne :

| **Fonction Composée** | **Dérivée** | **Condition** |
|---|---|---|
| $\mathbf{e^{u(x)}}$ | $\mathbf{e^{u(x)} \cdot u'(x)}$ | $u$ dérivable sur $\mathbb{R}$ |

**Exemple :** Soit $g(x) = e^{2x}$.

- $u(x) = 2x$
- $u'(x) = 2$
- Donc : $g'(x) = 2e^{2x}$

#### Primitive

| **Fonction** | **Primitive** | **Domaine** |
|---|---|---|
| $\mathbf{e^x}$ | $\mathbf{e^x + C}$ | $\mathbb{R}$ |

---

### 🔄 Fonction Réciproque

La fonction exponentielle est injective sur $\mathbb{R}$.

La fonction réciproque est la **fonction logarithme népérien**, notée $\ln$ :

$$\ln : ]0, +\infty[ \to \mathbb{R}$$

Elle vérifie :
$$\forall x > 0, \quad \ln(e^x) = x$$

**Graphiquement :** Les courbes de $e^x$ et $\ln(x)$ sont symétriques par rapport à la droite $y = x$.

---

### 🌊 Développements et Séries

#### Série de Taylor/Maclaurin

$$e^x = \sum_{n=0}^{+\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots$$

Cette série converge pour $x \in \mathbb{R}$.

#### Formule d'Euler (si applicable)

$$e^{i\theta} = \cos(\theta) + i \sin(\theta)$$

---

### 📈 Variations et Représentation Graphique

#### Tableau de Variations

| $x$ | $-\infty$ |  | $0$ |  | $+\infty$ |
|---|---|---|---|---|---|
| $f'(x)$ |  | $+$ |  | $+$ |  |
| $f(x)$ | $0$ | $\nearrow$ | $1$ | $\nearrow$ | $+\infty$ |

#### Points Remarquables

- **Extrema locaux** : Aucun.
- **Points d'inflexion** : Aucun.
- **Asymptotes** :
  - Horizontale : $y = 0$ (en $-\infty$).

---

### 🎯 Applications et Contextes

[DESCRIPTION DES APPLICATIONS PRATIQUES]
La fonction exponentielle modélise des phénomènes de croissance ou décroissance exponentielle, comme la radioactivité, la croissance bactérienne, ou les intérêts composés en finance.

**Domaines d'application :**
- **Biologie** : Croissance de populations.
- **Physique** : Décroissance radioactive.
- **Finance** : Calcul des intérêts composés.

**Modélisation :** Cette fonction permet de modéliser des phénomènes où la variation est proportionnelle à la quantité présente.

### 💡 Remarques et Astuces

> [!tip] Astuce de Calcul
> Pour calculer $e^{a+b}$, on peut utiliser la propriété $e^{a+b} = e^a \cdot e^b$.

> [!warning] Attention
> La fonction exponentielle n'est pas périodique, contrairement aux fonctions trigonométriques.

> [!info] Rappel Important
> La dérivée de $e^x$ est $e^x$ pour tout $x \in \mathbb{R}$.

---

#Fonction/Exponentielle #Analyse #Mathématiques