# Introduction aux bases de données

## Objectifs du cours

Ce cours a pour objectif l’étude des principes des SGBD relationnels et la mise en pratique de ces principes. Le contenu du cours est essentiellement le suivant :

- Les concepts de base des bases de données relationnelles. Il s'agit de présenter les concepts ainsi que l'algèbre relationnelle.
- Langages d’interrogation et de manipulation. L’accent est mis sur SQL et ses fondements.
- Conception d’un schéma relationnel. Il s’agit de savoir définir un schéma relationnel complet et correct, comprenant des tables, des contraintes, des vues.

Des travaux pratiques avec le SGBD SQLite permettent de mettre en œuvre les techniques étudiées en cours. L’accent est donc mis sur les notions de base (qu’est-ce qu’un SGBD, qu’une base de données, qu’un langage d’interrogation) et leur application pratique.

## Compétences visées

Il est demandé d’avoir acquis à la fin du cours les connaissances nécessaires à l’utilisation d’un SGBD par un informaticien non spécialiste :

- création d’un schéma ;
- insertion ;
- mise-à-jour ;
- destruction ;
- interrogation de données.

## Équipe pédagogique

- Damien Pellier – [Damien.Pellier@univ-grenoble-alpes.fr](mailto:Damien.Pellier@univ-grenoble-alpes.fr)
- ...

## Modalités de contrôle de connaissances

- **Note finale :** **15% CC et 85% examen final**  
- **ECTS :** 6  
- **Volume horaire :** 10h de cours, 10h de TD et 10h de TP

!!! danger "IMPORTANT"
    - Tous **les travaux pratiques** sont à réaliser en binôme et **comptent pour votre note de CC**.  
    - **Le même binôme fait tous les TP ensemble** (pas de divorce pendant le semestre).  
    - Tous les sujets de TP et de TD sont disponibles dès la première séance de cours.  
    - **En cas de retard ou de non-rendu, la note de 0 sera attribuée**.  
    - Les TPs sont à rendre **au plus tard le jour du TP** au format papier à votre enseignant.

## Plan du cours

| Supports de cours | TD | TP | Ressources |
|-------------------|----|----|------------|
| **Partie n°1 : Introduction aux bases de données relationnelles** ||||
| [Cours n°1: Concepts des bases de données relationnelles](databases/01.introduction.pdf) | [TD n°1](databases/td01.pdf) | | |
| [Cours n°2: L'algèbre relationnelle](databases/02.algebre.pdf) | [TD n°2](databases/td02.pdf) | [TP n°1](databases/tp01.pdf) | [BD TP n°1](databases/le_grand_bazard.bd) |
| **Partie n°2 : Utilisation des bases de données relationnelles** ||||
| [Cours n°3: SQL DML (1)](databases/03.SQL1.pdf) | [TD n°3](databases/td03.pdf) | [TP n°2](databases/tp02.pdf) | [BD TP n°2](databases/les_employes.bd) |
| [Cours n°4: SQL DML (2)](databases/04.SQL2.pdf) | [TD n°4](databases/td04.pdf) | [TP n°3](databases/tp03.pdf) | [BD TP n°3](databases/agence_de_voyages.bd) |
| [Cours n°5: SQL DDL](databases/05.SQL3.pdf) | [TD n°5](databases/td05.pdf) | [TP n°4](databases/tp04.pdf) | |
| **Développement des bases de données relationnelles** ||||
| [Cours n°6: Modèle entité-associations](databases/06.entite.pdf) | [TD n°6](databases/td06.pdf) | | |
| [Cours n°7: Élaboration d'un schéma conceptuel](databases/07.conception.pdf) | [TD n°7](databases/td07.pdf) | | |
| [Cours n°8: Production du schéma de base de données](databases/08.production.pdf) | [TD n°8](databases/td08.pdf) | | |

## Ressources

- [Précis de traduction de l'algèbre relationnelle au SQL](databases/precis-ar-sql.pdf)

## Les travaux pratiques

Les travaux pratiques seront à réaliser avec l'outil [SQLiteStudio](http://sqlitestudio.pl).  
Pour l'installer, téléchargez la version adaptée à votre système d'exploitation dans la section [téléchargement](http://sqlitestudio.pl/?act).

SQLiteStudio est un éditeur graphique simple de requêtes qui fonctionne sur le moteur de base de données [SQLite](http://www.sqlite.org), une bibliothèque open source en C respectant les propriétés **ACID** et implémentant le standard **SQL-92**. Elle ne nécessite aucun serveur, car tout est contenu dans un fichier local.

La documentation complète est accessible ici : [Documentation officielle SQLite](http://www.sqlite.org/docs.html).

!!! tip "FAQ TPs"
    - Consultez la [FAQ sur les TPs](databases/faqtp.md). Elle sera enrichie au fil de vos questions.

## Références bibliographiques

- *Introduction aux Bases de Données*, C. Date, Vuibert, 2004  
- *Bases de Données*, G. Gardarin, Eyrolles, 2003  
- *SQL 2 De la théorie à l’application*, P. Delmal, De Boeck Université, 1998
