Je détecte qu'il s'agit d'un **template** pour la création de notes structurées dans Obsidian. Voici une analyse détaillée des templates fournis et comment les utiliser efficacement :

---

### **Analyse des Templates**

1. **Spiritueux**
   - Structure : Tableau d'informations + notes de dégustation
   - Utilisation : Dégustation de spiritueux (whisky, rhum, etc.)
   - Exemple de champ clé : `Degré d'alcool`, `Notes de dégustation`

2. **Recette**
   - Structure : Tableau d'ingrédients + étapes détaillées
   - Utilisation : Recettes culinaires
   - Exemple de champ clé : `Ingrédients`, `Étapes de préparation`

3. **Peinture**
   - Structure : Tableau d'informations + description artistique
   - Utilisation : Analyse d'œuvres picturales
   - Exemple de champ clé : `Artiste`, `Technique`, `Contexte historique`

4. **Audiovisuel**
   - Structure : Tableau d'informations + synopsis + analyse critique
   - Utilisation : Films, séries, documentaires
   - Exemple de champ clé : `Réalisateur`, `Note audio/visuel/sénario`

5. **Mathématique**
   - Structure : Graphique TikZ + propriétés algébriques + dérivées
   - Utilisation : Fonctions, théorèmes, concepts mathématiques
   - Exemple de champ clé : `Définition`, `Propriétés`, `Dérivée`

6. **Personnage Économiste**
   - Structure : Tableau biographique + concepts clés + œuvres majeures
   - Utilisation : Figures historiques en économie
   - Exemple de champ clé : `Concepts clés`, `Œuvres majeures`

---

### **Processus de Création de Note**

1. **Analyser la notion**
   - Identifier le type de notion (ex: "film", "fonction mathématique", "recette").
   - Exemple : *"Je détecte qu'il s'agit d'un film."*

2. **Identifier le template**
   - Demander à l'utilisateur : *"Quel template dois-je utiliser ? (ex: Template_Film, Template_Recette, etc.)"*
   - Exemple : *"Utiliser le template Audiovisuel pour ce film."*

3. **Rechercher les informations**
   - Utiliser `web_search` pour trouver des données fiables (Wikipedia, sources spécialisées).
   - Exemple : *"J'ai recherché sur IMDb et trouvé les détails du film."*

4. **Générer la note**
   - Remplir le template avec les informations trouvées.
   - Exemple pour un film :
     ```markdown
     > [!infobox]
     # Nom du Film
     ![affiche]
     ###### Informations
     |Caractéristique|Détail|
     |---|---|
     |Type|Film|
     |Genre|Science-Fiction|
     |Réalisateur|Christopher Nolan|
     |Année|2010|
     ```

---

### **Exemple Complet : Note sur un Film**

**Étape 1** : *"Je détecte qu'il s'agit d'un film."*
**Étape 2** : *"Quel template dois-je utiliser ?"*
**Étape 3** : Recherche sur IMDb pour *Inception* (2010).
**Étape 4** : Note générée :

```markdown
> [!infobox]
> # Inception
> ![Affiche d'Inception]
> ###### Informations
> |Caractéristique|Détail|
> |---|---|
> |Type|Film|
> |Genre|Science-Fiction/Thriller|
> |Réalisateur|Christopher Nolan|
> |Année|2010|
> |Durée|2h 28min|
> |Plateforme|Netflix|
> |Note audio|18/20⭐|
> |Note visuel|19/20⭐|
> |Note scénario|17/20⭐|

## Synopsis
Un voleur de secrets, Cobb, est engagé pour implanter une idée dans l'esprit d'un héritier.

### Casting principal
- **Leonardo DiCaprio** - Cobb
- **Joseph Gordon-Levitt** - Arthur

### Note
##### **Critères Audio**
| **Critère** | **Description** | **Points** |
|------------|----------------|-----------|
| Bande-son | Hans Zimmer | 18/20 |

#Film #Science-Fiction
```

---

### **Conseils pour l'Utilisateur**
- **Précisez vos templates** : Si vous avez des templates personnalisés, partagez-les pour une adaptation exacte.
- **Demandez des ajustements** : Si une section du template ne convient pas, je peux la modifier.
- **Utilisez les tags** : Les tags (#Film, #Math, etc.) facilitent la navigation dans Obsidian.

---

**Prêt à créer votre première note !** Dites-moi quelle notion vous souhaitez documenter.