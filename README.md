# L'influence de l'âge dans le football professionnel (LDC 2023-2024)

Ce dépôt contient le projet d'analyse statistique réalisé dans le cadre du cursus d'Économie Internationale et Développement à l'Université Paris-Dauphine (L3 EID). L'étude explore la mesure dans laquelle l'âge des joueurs de football de haut niveau conditionne leurs performances et leur positionnement sur le terrain.

## Présentation du Projet
L'objectif est d'analyser l'impact de l'âge à travers plusieurs indicateurs clés de performance en prenant comme cadre d'étude la **Ligue des Champions de l'UEFA (saison 2023-2024)**, permettant ainsi de comparer des athlètes évoluant au plus haut niveau européen.

### Données & Échantillonnage
* **Sources :** Données collectées sur les plateformes officielles *FBref* et *WhoScored*.
* **Population globale :** +2 000 joueurs (incluant les feuilles de match pour intégrer l'impact de la vie de vestiaire).
* **Échantillon :** Tirage aléatoire simple sans remise de **200 joueurs** ($X_i \sim \text{i.i.d.}$).

## Variables Étudiées
1. **L'âge (Quantitative discrète) :** Variable pivot de l'étude (Moyenne observée : ~27.26 ans).
2. **Le poste (Qualitative nominale) :** Réparti en 4 catégories (Attaquants, Milieux, Défenseurs, Gardiens).
3. **Le temps de jeu (Quantitative discrète) :** Reflet de la régularité et des choix tactiques.
4. **Le pourcentage de passes réussies (Quantitative discrète) :** Indicateur de la performance technique globale.

## Méthodologie & Tests Statistiques
Le projet implémente différents outils d'analyse statistique et économétrique sous **R** :

* **Estimation de la moyenne d'âge :** Ponctuelle et par Intervalle de Confiance (IC à 95% : `[26.68 , 27.85]`).
* **Test de conformité (t-test unilatéral) :** Comparaison du taux de passes réussies en LDC face à la Premier League (Validation d'une performance technique supérieure en LDC au seuil de 5%).
* **Comparaison de caractéristiques théoriques :**
  * *Test d'égalité des moyennes (Welch Test) :* Analyse de la différence d'âge moyenne entre milieux (profils plus jeunes/dynamiques) et défenseurs (profils plus matures/expérimentés).
  * *Test d'égalité des variances (F-test) :* Analyse de la dispersion du temps de jeu entre attaquants et défenseurs.
* **Test d'indépendance du Chi-deux ($\chi^2$) :** Analyse de la contingence entre les classes d'âge et les postes occupés.

## Technologies & Librairies R
* **Langage :** R
* **IDE :** RStudio
* **Packages utilisés :** * `readxl` (Importation et gestion des bases de données)
  * Fonctions natives de tests (`t.test`, `var.test`, `chisq.test`)
