# FAQ TP

## SQLiteStudio

**Est-ce qu'il serait possible de nous faire part d'un guide d'utilisation de SQLiteStudio ?**

> Vous pouvez trouver toutes les informations nécessaires à l'utilisation de SQLiteStudio sur le site de [SQLiteStudio](https://sqlitestudio.pl/index.rvt?act=about) dans l'onglet wiki. En particulier, vous trouverez :
>
> - [Le manuel d'utilisation de SQLiteStudio](https://github.com/pawelsalawa/sqlitestudio/wiki/User_Manual)
> - [Une FAQ](https://github.com/pawelsalawa/sqlitestudio/wiki/FAQ)
> - [Des scripts](https://github.com/pawelsalawa/sqlitestudio/wiki/Scripts_repository)
> - [Des astuces](https://github.com/pawelsalawa/sqlitestudio/wiki/Tips_&_Tricks)

> Pour ceux qui préfèrent une vidéo, je vous conseille [cette vidéo YouTube](https://www.youtube.com/watch?v=mK6Iy3HSyU4).

---

## TP1 : Le grand bazar

### Question 8

**Pourquoi la requête ci-dessous est-elle fausse ?**

```sql
SELECT NPRO, NOMC, NOMF
FROM ACHAT, PRODUIT, VENTE
WHERE NPRA = NPRO AND NPRV = NPRO
GROUP BY NPRO
```

> On vous demande de donner pour chaque produit, les noms des fournisseurs du produit et les noms des clients l’ayant acheté, i.e., pour les produits contenus dans la relation PRODUITS, les noms fournisseurs, et les noms des clients. Il est donc faux et **inutile** dans cette requête de créer une partition sur NPRO.

---

## TP2 : Les employés

### Question 2

**On demande les niveaux de salaire (sans doublons) ou tous les salaires (donc avec des doublons) ?**

> Il faut fournir pour chaque employé son salaire. Il est possible que plusieurs employés aient le même salaire.

### Question 3

**J'ai utilisé un DISTINCT pour ne pas avoir les doublons. Faut-il ou non mettre un DISTINCT dans la première partie du sujet ou rajouter les prénoms dans la seconde ?**

> Il n'est pas nécessaire de mettre un DISTINCT. On vous demande tous les salaires perçus par tous les employés. Comme EMPNO est la clé primaire, il n’y a pas de doublons. Vous pouvez ajouter NOM si vous le souhaitez.

### Question 5

**Pour les variantes de la question 5, est-ce que ces requêtes sont justes ?**

#### Variante A

```sql
SELECT DISTINCT ENAME AS NAME, SAL
FROM EMP
WHERE ENAME LIKE 'M%' AND SAL > 1290
ORDER BY [ASC];
```

> Non, la syntaxe de la clause `ORDER BY` est incorrecte. Il manque l'attribut, et les crochets ne sont pas valides.

#### Variante B

```sql
SELECT DISTINCT ENAME AS NAME, SAL
FROM EMP
WHERE ENAME LIKE 'M%' AND SAL > 1290
ORDER BY [DESC];
```

> Idem que ci-dessus.

#### Variante C

```sql
SELECT DISTINCT ENAME AS NAME, SAL
FROM EMP
WHERE ENAME LIKE 'M%' AND SAL > 1290
ORDER BY SAL DESC;
```

> La requête est juste.

**Faut-il toujours prendre les noms commençant par 'M' ?**

> Oui, dans toutes les variantes, seuls les noms commençant par 'M' doivent être sélectionnés.

### Question 6

**Doit-on donner le numéro ou le nom des départements ?**

> Le numéro suffit, mais le nom peut rendre le résultat plus lisible.

**Les départements doivent-ils contenir les 3 postes à la fois ?**

> Oui, les 3 à la fois (ET logique).

**Faut-il indiquer les chefs seulement ou aussi les employés percevant des commissions ?**

> Seulement les chefs, comme demandé. Les requêtes doivent être indépendantes des données actuelles de la base.

### Question 9

**Doit-on prendre en compte les commissions ou juste le salaire ?**

> Les deux approches sont acceptées.

### Question 10

**Comment afficher la hiérarchie de l'entreprise ?**

> Utilisez une requête récursive ou une approche en niveaux successifs avec jointures.

**Format attendu :**

```
HIERARCHIE(ENAME, NIVEAU)
```

> Par exemple, King est au niveau 1.

**Pourquoi ma vue récursive est refusée ?**

```sql
CREATE VIEW HIE(EMPNO,ENAME,MGR,NIV) AS
SELECT EMPNO,ENAME,MGR,1 NIV
FROM EMP
WHERE MGR IS NULL
UNION ALL
SELECT E.EMPNO, E.ENAME, E.MGR, '_'+1 NIV
FROM EMP E
INNER JOIN HIE ON E.MGR = HIE.EMPNO
WHERE E.MGR IS NOT NULL
```

> Une vue ne peut pas être récursive dans SQLite. Faites des vues séparées pour chaque niveau et utilisez `UNION`.

**La hiérarchie est-elle équivalente au grade ?**

> Non, elle est basée sur le champ `MGR` (manager), pas `GRADE`.

**Pourquoi ma requête est-elle fausse ?**

```sql
SELECT DISTINCT e1.ENAME
FROM EMP e1, EMP e2
WHERE e1.EMPNO = e2.MGR
ORDER BY e2.MGR > e1.MGR
```

> 1. La syntaxe `ORDER BY` est incorrecte.
> 2. Elle affiche les noms des employés qui sont des managers, pas la hiérarchie.

**Et si ma requête ne s’adapte pas à un changement de niveau ?**

> C’est une limite de SQLite. Si votre dernière union ne contient qu’un employé au lieu de deux, c’est une erreur (p. ex. GROUP BY inutile).

---

## Questions diverses

**Doit-on refaire les questions d’algèbre relationnelle ?**

> Non, seulement la partie 5 est à rendre. Vous pouvez refaire les autres pour réviser.

**Faut-il afficher les résultats des requêtes SQL dans la partie 1 ?**

> Oui.

**Dans la partie 2, faut-il afficher les résultats déjà vus en partie 1 ?**

> Non, ce n’est pas nécessaire.

---

## TP3 : L’agent de voyage

### Question 7

**Doit-on tenir compte des circuits ayant lieu à la même date ?**

> Non, la date n’intervient pas ici.

### Question 8

**Faut-il prendre en compte les deux cas (monuments ou aucun) ?**

> Non, seulement les circuits qui passent par des monuments.

### Question 9

**Comment tester ma requête sans circuits multi-pays ?**

> Ajoutez temporairement un circuit multi-pays à la base. Supprimez-le après test.

### Question 12

**Faut-il uniquement les circuits entièrement en France ?**

> Non, un seul passage en France suffit.

### Question 13

**Le coût des monuments est-il déjà inclus ?**

> Oui.

**Doit-on calculer le revenu total à partir des programmations ou des réservations ?**

> À partir des réservations. Le nombre de places disponibles ne reflète pas les ventes réelles.

### Question 14

**(Suite à une coupure du texte)**

> Le prix des visites des monuments est déjà inclus. Il ne sert à rien de les rajouter.
