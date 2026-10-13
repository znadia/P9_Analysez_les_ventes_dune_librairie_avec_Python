# P9 Analysez les ventes d'une librairie avec Python

L’entreprise et les données sont fictives.

## Contexte

Lapage est une librairie historiquement physique qui a ouvert son site de vente en ligne il y a 2 ans. Le responsable commercial souhaite faire le point sur l'activité pour décider des prochaines actions (nouvelles offres, prix, ciblage de la clientèle). J'ai nettoyé et fusionné les données de ventes avec Python, calculé les indicateurs clés, puis testé statistiquement le lien entre le profil des clients et leur comportement d'achat.

## Objectifs

- Vérifier la qualité des données et préparer une table unique prête pour l'analyse
- Calculer et visualiser les indicateurs de vente (chiffre d'affaires, volumes, tops et flops)
- Analyser la concentration du chiffre d'affaires et repérer les clients professionnels
- Tester 5 corrélations entre le profil des clients et leurs achats
- Présenter les résultats à un public non technique

## Réalisations

- Nettoyage de 3 fichiers (clients, produits, transactions) et suppression de 361 041 lignes entièrement vides
- Fusion des fichiers en une table de 687 534 transactions sans valeur manquante
- Repérage de 21 clients sans achat et de 21 produits jamais vendus, isolés et documentés
- Identification de 4 comptes professionnels (B2B) avec un seuil justifié, après avoir écarté la méthode IQR qui en repérait 608
- Évolution du chiffre d'affaires mensuel avec moyennes mobiles (12 M€ sur 2 ans)
- Analyse du chiffre d'affaires et des volumes par catégorie, tops et flops des produits
- Courbe de Lorenz et indice de Gini (0,442 pour tous les clients, 0,398 hors B2B)
- Tests statistiques sur 5 corrélations avec hypothèses H0 et H1, test de normalité de Kolmogorov-Smirnov, puis Chi-2, Spearman ou Kruskal-Wallis selon les cas
- Calcul de la taille d'effet (V de Cramér) pour ne pas se limiter à la p-value
- Support de présentation avec recommandations pour la direction

## Résultats clés

- 4 comptes B2B représentent 7,4 % du chiffre d'affaires
- Le genre n'a quasiment aucun lien avec la catégorie achetée (V de Cramér = 0,006)
- L'âge est fortement lié à la taille du panier moyen (Spearman = -0,70)
- La catégorie 2 attire un public nettement plus jeune (24 ans en médiane contre 42 et 46 ans)

## Outils

Python, pandas, NumPy, SciPy, Matplotlib, Seaborn, Plotly, Google Colab

## Compétences

- Nettoyer, fusionner et contrôler la qualité de données issues de plusieurs fichiers
- Calculer des indicateurs de vente et les visualiser
- Choisir et appliquer un test statistique adapté au type de variables
- Interpréter une p-value et une taille d'effet
- Détecter des valeurs aberrantes et justifier un choix méthodologique
- Restituer une analyse à un public non technique

## Fichiers

- `notebook_analyse_ventes.ipynb` notebook complet avec le nettoyage, les analyses et les tests statistiques
