```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}

\begin{document}
\begin{tikzpicture}
\begin{axis}[
    axis lines=middle,
    grid=both,
    domain=0.1:10,
    samples=200,
    xlabel={$x$},
    ylabel={$f(x)$},
    width=10cm,
    height=8cm
]
\addplot[blue, thick] {ln(x)};
\end{axis}
\end{tikzpicture}
\end{document}
```

## 💡 Qu'est-ce que la fonction logarithme ?

### Intuition et contexte

La fonction logarithme, notée **$\ln(x)$** ou **$\log_b(x)$**, émerge naturellement lorsqu'on cherche à répondre à la question : *"Combien de fois faut-il multiplier 1 par un nombre pour obtenir x ?"*. Cette notion est née de l'étude des exponentielles et de la nécessité de résoudre des équations comme $a^y = x$.

Imaginez que vous ayez une population qui double chaque année. Le logarithme vous permet de savoir après combien d'années vous atteindrez une certaine taille. C'est un outil fondamental pour transformer des multiplications en additions, ce qui simplifie énormément les calculs.

### Définitions selon le contexte

> [!abstract] Définition exponentielle (définition fondamentale)
> La fonction logarithme est la fonction réciproque de l'exponentielle. Pour une base $b > 0$, $b \neq 1$, on définit :
> $$ \log_b(x) = y \iff b^y = x $$

> [!abstract] Définition par intégrale (définition analytique)
> Pour la base $e$, le logarithme naturel est défini par :
> $$ \ln(x) = \int_1^x \frac{1}{t} dt $$

Ces deux définitions sont équivalentes car l'exponentielle et le logarithme sont des fonctions réciproques l'une de l'autre.

---

## 🔍 Comment ça fonctionne ?

### L'idée centrale

Le logarithme mesure la taille d'un nombre en termes d'exposants. Par exemple, $\log_2(8) = 3$ parce que $2^3 = 8$. C'est comme compter le nombre d'étapes nécessaires pour atteindre un certain niveau de croissance exponentielle.

Par exemple, si une bactérie double sa population chaque heure, $\log_2(1000)$ vous dira après combien d'heures vous aurez 1000 bactéries.

### Domaine et contraintes

La fonction logarithme est définie pour $x > 0$ parce que :
- On ne peut pas prendre le logarithme d'un nombre négatif (pas de racine réelle)
- Le logarithme de 0 n'existe pas (car $b^y = 0$ n'a pas de solution finie)
- Le logarithme de 1 est toujours 0, car $b^0 = 1$ pour tout $b > 0$

---

## 📊 Propriétés principales

### Propriété 1: Logarithme d'un produit

Le logarithme transforme les multiplications en additions :

$$ \log_b(xy) = \log_b(x) + \log_b(y) $$

**Pourquoi ?** Par définition, si $\log_b(x) = a$ et $\log_b(y) = c$, alors $b^a = x$ et $b^c = y$. Donc $xy = b^a \cdot b^c = b^{a+c}$. Ainsi, $\log_b(xy) = a + c = \log_b(x) + \log_b(y)$.

**Conséquence pratique:** Cette propriété permet de simplifier les calculs avec de grands nombres, comme en astronomie ou en finance.

---

### Propriété 2: Logarithme d'une puissance

Le logarithme d'une puissance est proportionnel à l'exposant :

$$ \log_b(x^n) = n \log_b(x) $$

**Pourquoi ?** Si $\log_b(x) = a$, alors $x = b^a$. Donc $x^n = (b^a)^n = b^{an}$. Ainsi, $\log_b(x^n) = an = n \log_b(x)$.

**Conséquence pratique:** Cette propriété est cruciale en chimie pour calculer les pH ou en acoustique pour les décibels.

---

### Propriété 3: Changement de base

On peut changer la base du logarithme sans changer sa valeur :

$$ \log_b(x) = \frac{\log_k(x)}{\log_k(b)} $$

**Pourquoi ?** Cette propriété vient du fait que le logarithme est une fonction réciproque de l'exponentielle. Elle permet de calculer des logarithmes avec n'importe quelle base à partir de la base naturelle ou décimale.

**Conséquence pratique:** Les calculatrices n'ont généralement que $\ln(x)$ et $\log_{10}(x)$, mais cette formule permet de calculer n'importe quel logarithme.

---

## 🧮 Calculs et manipulations

### Dérivée du logarithme naturel

La dérivée de $\ln(x)$ est particulièrement simple :

$$ \frac{d}{dx} \ln(x) = \frac{1}{x} $$

**Pourquoi cette formule?** Par définition, $\ln(x) = \int_1^x \frac{1}{t} dt$. La dérivée d'une intégrale est simplement la fonction intégrée.

**Pour les fonctions composées:** Si $u(x)$ est dérivable et positive, alors :
$$ \frac{d}{dx} \ln(u(x)) = \frac{u'(x)}{u(x)} $$

---

### Cas particuliers remarquables

| Valeur | Résultat | Pourquoi c'est intéressant |
|---|---|---|
| $\log_b(1)$ | $0$ | Car $b^0 = 1$ pour tout $b > 0$ |
| $\log_b(b)$ | $1$ | Car $b^1 = b$ |
| $\log_b(b^k)$ | $k$ | Propriété fondamentale des logarithmes |
| $\log_b(xy)$ | $\log_b(x) + \log_b(y)$ | Transformation des multiplications en additions |

---

## 🎯 Applications et exemples

### Exemple 1: Calcul du pH

**Contexte:** Le pH mesure l'acidité d'une solution. Il est défini comme $pH = -\log_{10}[H^+]$, où $[H^+]$ est la concentration en ions hydrogène.

**Problème:** Une solution a une concentration en ions hydrogène de $0.0001$ mol/L. Quel est son pH ?

**Résolution:**

1. On utilise la définition du pH :
   $$ pH = -\log_{10}(0.0001) $$

2. On calcule le logarithme :
   $$ \log_{10}(0.0001) = \log_{10}(10^{-4}) = -4 $$

3. On applique la formule du pH :
   $$ pH = -(-4) = 4 $$

**Interprétation:** Un pH de 4 correspond à une solution acide, comme le jus de citron.

---

### Exemple 2: Calcul du temps de doublement

**Contexte:** En finance, le temps nécessaire pour qu'un investissement double de valeur est donné par la formule :
$$ T = \frac{\ln(2)}{\ln(1 + r)} $$
où $r$ est le taux d'intérêt annuel.

**Problème:** Combien de temps faut-il pour qu'un investissement double avec un taux d'intérêt de 5% par an ?

**Résolution:**

1. On utilise la formule :
   $$ T = \frac{\ln(2)}{\ln(1.05)} $$

2. On calcule les logarithmes :
   $$ \ln(2) \approx 0.6931 $$
   $$ \ln(1.05) \approx 0.0488 $$

3. On divise :
   $$ T \approx \frac{0.6931}{0.0488} \approx 14.2 \text{ ans} $$

**Interprétation:** Il faut environ 14 ans pour que l'investissement double avec un taux d'intérêt de 5% par an.

---

## 🔗 Liens avec d'autres concepts

- **Exponentielle**: Le logarithme est la fonction réciproque de l'exponentielle, ce qui permet de résoudre des équations exponentielles.
- **Dérivée**: La dérivée du logarithme est $\frac{1}{x}$, ce qui en fait une fonction très utile en analyse.
- **Algorithmes**: Les logarithmes sont utilisés dans les algorithmes de recherche binaire et de tri rapide.
- **Échelle logarithmique**: Les graphiques en échelle logarithmique permettent de visualiser des données sur de grandes plages de valeurs.

---

## 📝 À retenir

> [!summary] L'essentiel
>
> La fonction logarithme est la réponse à la question "combien de fois faut-il multiplier 1 par un nombre pour obtenir x ?". Elle transforme les multiplications en additions, ce qui la rend extrêmement utile en mathématiques et dans les applications pratiques.
>
> La formule clé est $\log_b(xy) = \log_b(x) + \log_b(y)$, qui montre comment le logarithme transforme les produits en sommes.
>
> Le logarithme est défini pour $x > 0$ et sa dérivée est $\frac{1}{x}$, ce qui en fait une fonction fondamentale en analyse.

#Fonction/Logarithme #Analyse #Algorithmes #Finance