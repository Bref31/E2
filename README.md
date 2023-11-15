# Amélioration de l'Application de Diagnostic de Tumeurs Cérébrales par IA

## Introduction

Le domaine de la santé bénéficie de plus en plus des avancées technologiques, en particulier de l'intégration de l'intelligence artificielle (IA) dans le diagnostic médical. Le projet E2 s'inscrit dans cette dynamique d'innovation, visant à améliorer une application IA existante pour la prédiction de la présence et du type de tumeurs cérébrales à partir d'images radiologiques de cerveau. Ce projet s'appuie sur l'application originale disponible sur GitHub, offrant une base solide pour le développement et l'intégration de fonctionnalités avancées. Dans ce rapport, nous détaillerons le processus d'évaluation de l'application actuelle, l'analyse des performances du modèle pré-entraîné, les améliorations fonctionnelles intégrées, ainsi que les tests de régression pour garantir la fiabilité de l'application.

---

## Table des Matières

1. [Introduction](#introduction)
2. [Évaluation de l'Application Actuelle](#évaluation-de-lapplication-actuelle)
3. [Analyse de la Matrice de Confusion](#analyse-de-la-matrice-de-confusion)
4. [Améliorations Apportées à l'Application](#améliorations-apportées-à-lapplication)
5. [Tests de la Nouvelle Application](#tests-de-la-nouvelle-application)
6. [Discussion et Conclusion](#discussion-et-conclusion)
7. [Références](#références)
8. [Annexes](#annexes)

## Évaluation de l'Application Actuelle

La première étape dans l'amélioration de notre application a consisté à évaluer sa forme actuelle. L'application, construite sur un framework Flask, a été déployée dans un environnement de développement local. Toutes les dépendances nécessaires, telles que documentées dans le fichier `requirements.txt` sur le dépôt GitHub original, ont été installées. Le modèle pré-entraîné a été téléchargé et testé sur un ensemble de données distinctes pour garantir l'intégrité et la réplicabilité des résultats obtenus par le développeur initial.

## Analyse de la Matrice de Confusion et du Rapport de Classification

L'évaluation détaillée de la performance du modèle est essentielle pour comprendre ses capacités de prédiction et identifier les domaines nécessitant des améliorations. La matrice de confusion et le rapport de classification sont des outils statistiques qui nous aident à analyser l'efficacité du modèle. Voici une analyse des métriques extraites du rapport de classification :

- **Glioma Tumor**:
  - *Précision*: 0.89 - Le modèle a correctement prédit les gliomes 89% du temps lorsque son diagnostic était positif.
  - *Rappel*: 0.40 - Parmi tous les cas réels de gliomes, le modèle n'a identifié que 40% d'entre eux.
  - *F1-score*: 0.55 - Le score F1 pour les gliomes indique une balance entre la précision et le rappel qui est suboptimale, suggérant une marge d'amélioration dans la reconnaissance de cette classe spécifique.

- **Meningioma Tumor**:
  - *Précision*: 0.80 - Une précision solide indique que les prédictions positives du modèle pour le meningiome sont généralement fiables.
  - *Rappel*: 0.95 - Un rappel élevé démontre que le modèle est capable de détecter la majorité des cas réels de meningiomes.
  - *F1-score*: 0.87 - Ce score élevé reflète une performance bien équilibrée du modèle pour les meningiomes.

- **No Tumor**:
  - *Précision*: 0.65 - La précision plus faible pourrait indiquer des faux positifs, où le modèle prédit à tort l'absence de tumeur.
  - *Rappel*: 0.97 - Un rappel élevé signifie que le modèle est efficace pour identifier les scans sans tumeurs.
  - *F1-score*: 0.78 - Un F1-score assez élevé témoigne de l'efficacité du modèle dans la classification des cas sans tumeurs.

- **Pituitary Tumor**:
  - *Précision*: 0.98 - Indique que presque toutes les prédictions de tumeurs hypophysaires sont correctes.
  - *Rappel*: 0.73 - Suggère que le modèle a manqué environ un quart des cas réels de tumeurs hypophysaires.
  - *F1-score*: 0.84 - Un score F1 élevé montre que le modèle est fiable pour la détection de tumeurs hypophysaires.

- **Général**:
  - *Précision Globale*: 0.77 - Environ 77% des prédictions toutes classes confondues étaient correctes.
  - *Moyenne Macro*: 0.83 (précision), 0.76 (rappel), 0.76 (F1-score) - Des moyennes macro qui indiquent une bonne performance générale du modèle.
  - *Moyenne Pondérée*: 0.82 (précision), 0.77 (rappel), 0.76 (F1-score) - Ces moyennes pondérées tiennent compte du support de chaque classe et suggèrent que le modèle fonctionne bien, surtout pour les classes les mieux représentées dans l'ensemble de données.

Ces métriques indiquent que le modèle est très performant dans la détection de certaines classes de tumeurs, mais il pourrait être amélioré en termes de sensibilité aux gliomes. Les sections suivantes du rapport exploreront les améliorations possibles et les tests effectués pour valider l'efficacité de ces changements.

## Améliorations Apportées à l'Application

*[Expliquez ici les améliorations spécifiques que vous avez apportées à l'application, telles que l'intégration du modèle YOLO, l'ajout d'autres modèles de prédiction, et les mises à jour de l'interface utilisateur.]*

## Tests de la Nouvelle Application

*[Décrivez les tests de régression effectués et présentez les métriques d'évaluation de la nouvelle IA par rapport à l'ancien modèle.]*

## Discussion et Conclusion

*[Résumez les améliorations et leur impact, discutez des limites rencontrées et des perspectives d'évolution de l'application.]*

## Références

*[Listez toutes les références bibliographiques utilisées dans votre rapport.]*

## Annexes

*[Incluez tout code supplémentaire, captures d'écran, et autres ressources qui appuient votre rapport.]*

