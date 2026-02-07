# Template : personnages-artiste
## Règles de génération
Adapter le contenu à l'importance de l'artiste :
- Artiste mineur : biographie courte, 3-5 œuvres, style résumé
- Artiste majeur : biographie développée, 8-12 œuvres, analyse stylistique approfondie

Adapter le vocabulaire à la discipline :
- Peinture : "tableau", "toile", "fresque", "technique", "palette"
- Musique : "composition", "opus", "mouvement", "tonalité"
- Littérature : "roman", "poème", "essai", "style", "thèmes"
- Sculpture : "statue", "bas-relief", "marbre", "bronze"
- Architecture : "édifice", "plan", "style", "commande"

Distinguer la discipline principale si polyvalent (ex: Léonard = peintre + ingénieur).
Utiliser les liens wiki [[Nom]] pour œuvres, mouvements, contemporains.
## Propriétés (front matter YAML)
```yaml
---
aliases: [Leonardo di ser Piero da Vinci, Leonardo da Vinci]
tags: #art/personne/peinture #art/personne/ingénierie
nationalite: Italienne
discipline: peinture, ingénierie, anatomie, architecture
mouvement: Renaissance italienne
periode: Renaissance
image: https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Leonardo_da_Vinci_-_Self_Portrait.jpg/300px-Leonardo_da_Vinci_-_Self_Portrait.jpg
date_creation: 1452-1519
---
```

## Structure du document

### 1. Léonard de Vinci
**Type de bloc** : infobox

**Instructions** :
Dates : format "JJ mois AAAA - JJ mois AAAA" (v. si incertain).
Discipline : art(s) pratiqué(s).
Mouvement : courant principal, peut en avoir plusieurs.
Formation : où/avec qui il a appris.
Œuvre majeure : 1-2 œuvres les plus connues.
Max 50 car. par valeur.

**Format attendu de l'infobox** :
```
> [!Infobox]
> Léonard de Vinci
> ![[https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Leonardo_da_Vinci_-_Self_Portrait.jpg/300px-Leonardo_da_Vinci_-_Self_Portrait.jpg|300]]
>- **Dates** : 14 avril 1452 - 2 mai 1519
>- **Discipline** : peinture, ingénierie, anatomie, architecture
>- **Mouvement** : Renaissance italienne
>- **Formation** : atelier d'Andrea del Verrocchio
>- **Œuvre majeure** : La Joconde
```

**Champs a remplir** :
- Dates: 14 avril 1452 - 2 mai 1519
- Discipline: peinture, ingénierie, anatomie, architecture
- Mouvement: Renaissance italienne
- Formation: atelier d'Andrea del Verrocchio
- Œuvre majeure: La Joconde
- Image: https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Leonardo_da_Vinci_-_Self_Portrait.jpg/300px-Leonardo_da_Vinci_-_Self_Portrait.jpg

---

### 2. Biographie
**Type de bloc** : texte

**Instructions** :
Parcours chronologique : origines, formation, carrière, fin de vie.
2-4 paragraphes selon l'importance.
Mentionner :
- Origines familiales (milieu artistique ? mécénat ?)
- Formation (atelier, académie, autodidacte, maîtres)
- Voyages importants (influence sur le style)
- Mécènes et commandes majeures
- Vie personnelle si influence sur l'œuvre
- Circonstances de la mort

Léonard de Vinci naît le 14 avril 1452 à Vinci, en Toscane, d'une relation illégitime entre Caterina di Meo Lippi, une paysanne, et Pierre de Vinci, un notaire. Élevé par ses grands-parents paternels, il est inscrit à Florence dans une scuola d'abaco puis dans l'atelier d'Andrea del Verrocchio vers 1464. Il y côtoie des artistes comme Botticelli et Le Pérugin. En 1482, il quitte l'atelier et se présente au duc de Milan Ludovic Sforza comme ingénieur. Il y développe ses talents de peintre, ingénieur et scientifique, étudiant les mathématiques et le corps humain. En 1499, il part pour Mantoue, Venise puis Florence, où il travaille pour César Borgia. De 1506 à 1511, il est « peintre et ingénieur ordinaire » de Louis XII à Milan. En 1516, François Ier l'invite en France, où il s'installe au Clos Lucé. Il y meurt le 2 mai 1519, laissant derrière lui des œuvres majeures comme La Joconde.

---

### 3. Style et technique
**Type de bloc** : texte

**Instructions** :
2-3 paragraphes décrivant :
- Caractéristiques reconnaissables (couleurs, formes, thèmes, techniques)
- Évolution du style (périodes, tournants)
- Innovations apportées
- Influences reçues (maîtres, courants, voyages)
- Comparaison avec contemporains si pertinent

Léonard de Vinci se distingue par son approche scientifique de l'art, combinant observation minutieuse et innovation technique. Ses peintures, comme La Joconde, utilisent le sfumato, une technique de modelage des formes par des transitions subtiles de tons et de couleurs. Il étudie l'anatomie humaine et la perspective pour donner à ses œuvres une profondeur et un réalisme inédits. Son style évolue vers une complexité croissante, avec des compositions dynamiques et des expressions humaines subtiles. Influencé par Verrocchio et les maîtres florentins, il influence à son tour des générations d'artistes par son approche polymathe.

---

### 4. Œuvres principales
**Type de bloc** : section

**Instructions** :
Organiser par période ou par type selon pertinence.
Format :

> [!artwork] **Période / Type**
>
> - **`[[Titre de l'œuvre]]`** (date) — {{technique/genre}}, {{localisation si connue}}
>   {{description courte : sujet, importance, particularité}}
>
> - **`[[Titre de l'œuvre 2]]`** (date) — {{technique/genre}}
>   {{description courte}}

5-12 œuvres selon l'importance de l'artiste.
Mettre les chefs-d'œuvre en premier.
Pour la musique : mentionner opus, tonalité.
Pour la littérature : mentionner genre, thèmes.

> [!artwork] **Peintures majeures**
>
> - **`[[La Joconde]]`** (v. 1503-1519) — huile sur bois de peuplier, Musée du Louvre
>   Portrait emblématique de la Renaissance, célèbre pour son sfumato et son sourire énigmatique.
>
> - **`[[La Cène]]`** (1495-1498) — peinture murale à secco, Santa Maria delle Grazie, Milan
>   Représentation iconique du dernier repas du Christ, innovante par sa composition et sa perspective.
>
> - **`[[L'Homme de Vitruve]]`** (v. 1490) — dessin, Accademia, Venise
>   Étude des proportions humaines, symbole de l'harmonie entre l'homme et la nature.
>
> - **`[[La Vierge aux rochers]]`** (1483-1486) — huile sur bois, Louvre et National Gallery, Londres
>   Composition complexe avec des effets de lumière et des détails naturalistes.
>
> - **`[[Saint Jean-Baptiste]]`** (v. 1513-1516) — huile sur bois, Louvre
>   Dernière œuvre connue, marquée par une technique raffinée et une expression intense.

---

### 5. Influences et héritage
**Type de bloc** : section

**Instructions** :
Format :

> [!abstract] **Influences reçues**
> - `[[Artiste]]` : {{nature de l'influence}}
> - `[[Mouvement]]` : {{ce qu'il en a retenu}}

> [!example] **Influence exercée**
> - `[[Artiste/Mouvement]]` : {{comment il les a influencés}}
> - Postérité : {{impact durable sur l'art}}

Distinguer :
- Ce qu'il a reçu (maîtres, prédécesseurs, courants)
- Ce qu'il a transmis (élèves, disciples, mouvements postérieurs)

> [!abstract] **Influences reçues**
> - `[[Andrea del Verrocchio]]` : formation technique et artistique
> - `[[Renaissance italienne]]` : approche humaniste et scientifique de l'art

> [!example] **Influence exercée**
> - `[[Rafael]]` : adoption de techniques comme le sfumato
> - `[[Léonardisme]]` : mouvement artistique inspiré par ses innovations
> - Postérité : considéré comme l'archétype de l'artiste polymathe, influençant des générations d'artistes et scientifiques.

---

### 6. Chronologie
**Type de bloc** : chronologie

**Instructions** :
Liste chronologique des moments décisifs.
Format :
- **AAAA** : Événement (description courte)

Inclure :
- Naissance
- Début de formation
- Première œuvre notable
- Œuvres majeures
- Voyages importants
- Reconnaissance (prix, commandes prestigieuses)
- Mort

5-12 événements selon l'importance.

- **1452** : Naissance à Vinci, en Toscane.
- **1464-1482** : Apprentissage dans l'atelier d'Andrea del Verrocchio à Florence.
- **1482** : S'installe à Milan au service du duc Ludovic Sforza.
- **1495-1498** : Réalise La Cène à Milan.
- **1499** : Part pour Mantoue, Venise puis Florence.
- **1503-1519** : Travaille sur La Joconde.
- **1506-1511** : « Peintre et ingénieur ordinaire » de Louis XII à Milan.
- **1516** : S'installe en France à l'invitation de François Ier.
- **1519** : Mort au Clos Lucé, près d'Amboise.