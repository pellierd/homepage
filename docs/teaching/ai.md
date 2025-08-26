# Introduction à l'intelligence artificielle  

## Objectifs

Ce cours vise à familiariser les étudiants aux fondements de l'intelligence artificielle et de la robotique en s'appuyant sur la pédagogie par projet. Il vise également à les confronter aux difficultés de mise en œuvre afin de les rendre opérationnels au travers de la conception et du développement d'un robot ramasseur de balles en LEGO.

## Compétences visées

* Poser une démarche de résolution de problème,
* Implémenter les algorithmes classiques de l’intelligence artificielle,
* Maitriser les limites des algorithmes présentés en termes d’activités et de complexité,
* Maitriser les limites d’un système embarqué temps réel,
* Savoir concevoir les logiciels d’un robot autonome simple

## Descriptif de cours

L'intelligence artificielle cherche à rendre calculable des fonctions cognitives de haut niveau pour permettre le développement de robots autonomes d’un haut degré d'autonomie nécessitant peu ou pas de supervision. Le développement et le déploiement de robots à grande échelle aura un impact sociétal considérable si l’on pense aux applications qui en découleront. Ces robots pourraient devenir des compagnons crédibles dans notre vie quotidienne ou des substituts utiles dans des situations complexes, dangereuses ou gênantes. La clé de leur succès réside dans leur capacité à interagir avec l’homme. Même si ces systèmes sont encore hors de portée, ils participeront à la prochaine rupture technologique.

Dans ce cours nous présentons dans une première partie un panorama des techniques de base du domaine de l'intelligence artificielle et de la robotique.

Cet enseignement s’articule autour d’un enseignement théorique et d’un projet pratique se déroulant tout au long du semestre. Ce projet consiste à développer un robot autonome en LEGO pour résoudre une tâche complexe d’exploration, de cartographie et de collecte d’objets dans un environnement. A la fin du semestre, les étudiants seront amenés à comparer les performances de leurs robots respectifs au travers d'une compétition.

## Modalités de contrôle de connaissance

* **Note finale :** 100% projet
* **ECTS :** 6
* **Volume horaire :** 24h de cours et 24 de TD
* **Horaires :** Lundi 13H00-17H00 Fablab

## Notes sur l'organisation cours

!!!warning "Important"
    - Le cours est en présentiel au Fablab dans le bâtiment situé entre le bâtiment Ampère et la maison de l'INP.
    - La capacité d'accueil et le nombre de robots disponibles étant limité, l'option ne pourra accueillir plus de 35 étudiants. Aucun étudiant ne sera accepté s'il n'a pas été présent à la première séance de cours.
    - La présence est obligatoire.
    - Prévoir d'apporter un ordinateur, au moins pour 2 étudiants dans chaque groupe.
    - Le robot vous est prêté pour le semestre sous votre entière responsabilité.

## Plan du cours

| Semaine | Supports de cours                                  | TD                       | Ressources                                     |
|---------|----------------------------------------------------|--------------------------|------------------------------------------------|
| 1       | [Introduction à l'intelligence artificielle](ai/01_introduction.pdf) | [TD n°1](ai/td01.pdf)    | [Article Turing (1950)](ai/turing.pdf)          |
| 2       | [Les agents intelligents](ai/02_agents_intelligents.pdf) | [TD n°2](ai/td02.pdf)    |                                                |
| 3       | [Les algorithmes classiques de recherche en IA](ai/03_recherche.pdf) | [TD n°3](ai/td03.pdf)    |                                                |
| 4       | [Les algorithmes et recherches heuristiques](ai/04_heuristique.pdf) | [TD n°4](ai/td04.pdf)    |                                                |
| 5       | [La programmation des jeux de réflexion](ai/05_jeux.pdf) | [TD n°5](ai/td05.pdf)    | [Article sur DeepBlue](ai/deepblue.pdf)        |
| 6       | [Le problème de satisfaction de contraintes](ai/06_csp.pdf) | [TD n°6](ai/td06.pdf)    |                                                |
| 7       | [Les agents logiques](ai/07_agent_logique.pdf)    | [TD n°7](ai/td07.pdf)    |                                                |
| 8       | [La logique du premier ordre](ai/08_logique.pdf)  | [TD n°8](ai/td08.pdf)    |                                                |
| 9       | [L'inférence en logique du premier ordre](ai/09_inference.pdf) | [TD n°9](ai/td09.pdf)    |                                                |
| 10      | [Introduction à la programmation logique avec Prolog](ai/10_prolog.pdf) | [TD n°10](ai/td10.pdf)   |                                                |
| 11      | [La planification automatique](ai/11_planification.pdf) | [TD n°11](ai/td11.pdf)   | [PDDL4J](http://pddl4j.imag.fr/)               |
| 12      | [L'apprentissage artificiel](ai/12_apprentissage.pdf) |                          |                                                |



## Projet de robotique

Le projet de robotique consiste à programmer un robot capable de ramasser un maximum de palets sur un plateaux en un minimum de temps. La forme des robots vous est imposée. L'évaluation consistera à opposer vos différents robots lors d'une compétition en semaine 12. Votre note de projet tiendra compte des évaluations hebdomadaires. Le projet est à réaliser par groupe de 4 ou 5. Le sujet détaillé du projet disponible [ici](project).

La librairie utilisée est [leJos](https://lejos.sourceforge.io/). Pour l'installation, veuillez vous référer à [cette vidéo YouTube](https://www.youtube.com/watch?v=NyoF0Ws6SkY).  Je mets également à votre disposition quelques exemples : [lejos_exemples.zip](ai/lejos_exemples.zip). Finalement, pour ceux qui veulent utiliser la caméra infrarouge pour détecter les palettes, vous pouvez vous appuyer sur [la description du protocole](ai/ir_camera.pdf) et le [code Java client fourni](ai/ev3client.java.zip).

!!!info "Remarque"
    Vous allez réaliser votre premier projet de développement pour la plupart à plusieurs. L'outil indispensable que vous devez utiliser est **Git**. Pour ceux qui ne sont pas familiarisés avec Git, je vous invite à réaliser [ce tutoriel](https://perso.liris.cnrs.fr/pierre-antoine.champin/enseignement/intro-git/). Pour configurer Git avec Eclipse, vous pouvez suivre [ce tutoriel](https://www.youtube.com/watch?v=mlN7VvZkXtM&ab_channel=Emds).



  | Groupe | Étudiants | GitHub |
  |--------|-----------|--------|
  | n°1 | Mathias Devilliers, Paul Ndong, Saliha Ozturk, Carole Mitton | [GitHub](https://github.com/MathiaasGH/wall-e-dmno) |
  | n°2 | ABDOUL KHADIR Diallo, BOUCQ-KIEFFEL Léna, DUBUS Roxane | [GitHub](https://github.com/kieffellena/Projet-IA-BDD) |
  | n°3 | Sara IKAN, Alix PRATABUY, Eva DROSZEWSKI, Anesie MARTINIANI | [GitHub](https://github.com/evaski/projet_sully_ia.git) |
  | n°4 | Adam Cotard, Quentin Juillat, Tom Laucournet, Tao Thill, Brice MC CARTHY | [GitHub](https://github.com/AdamInLoveOfBrice/miashsia/) |
  | n°5 | Basak Unal, Narta Neziraj, Yassmina Cherqaoui, Zoé Laget-Thomas | [GitHub](https://github.com/entjellybean/Ai-lojos-github) |
  | n°6 | Victor CHARREYRON, Thomas BEGOTTI, Alexander OSTLE, Flora MOULIN | [GitHub](https://github.com/thoms9/IntroIA_T_A_F_V) |
  | n°7 | TAMSOURI Mohammed, HALILY Youssef, NGUIRANE Marième, AMACHAT Yousra, AIT EL HADJ Anas | [GitHub](https://github.com/AnasAEA/Groupe-IA-Miashs-Proba) |


## Références bibliographiques

* S. Russell et P. Norvig, [**Artificial Intelligence: A Modern Approach**](ai/ai_book.pdf), Prentice Hall, 2002  
* J.-G. Ganascia, *L’intelligence artificielle*, Flammarion, 1993  
* I. Bratko, *Programmation en Prolog pour l’intelligence artificielle*, 2001  
* J. Alliot et T. Schiex, *Intelligence Artificielle et Informatique Théorique*, Cépaduès Editions, 1993  
* N. Nilsson, *Artificial Intelligence: A New Synthesis*, Morgan Kaufmann, 1998  
