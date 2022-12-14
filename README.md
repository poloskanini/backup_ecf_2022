![alt text](https://www.sngaf.com/wp-content/uploads/2022/09/STUDI-FITNESS-VISUEL-MAIL-1024x614.jpg)

# STUDI FITNESS

Projet réalisé dans le cadre de l'ECF Décembre 2022.


## Tech Stack

- **Frontend:** HTML / CSS / JavaScript / Bootstrap 5
- **Moteur de Template:** Twig
- **Backend:** PHP, Symfony 5.4.12
- **Base de données :** MySQL - MariaDB


## Authors

Nicolas Barthès
- [Github](https://github.com/poloskanini)
- [Portfolio](https://www.nicolasbarthes.com)


## Pré-Requis

- PHP >= 8.0
- Composer >= 2
- Npm (ou Yarn)
- MySQL - MariaDB
- WebPack Encore (JS / CSS)


<!-- ## Trello du projet
- [Trello](https://trello.com/b/CyZoe9QM) -->

<hr>

## Installation

Suivez les étapes ci-dessous pour installer localement mon projet et le tester.


### Cloner le projet

```bash
  git clone git@github.com:poloskanini/ecf_2022.git
```

### Aller dans le répertoire du projet

```bash
cd ecf_2022
```

## Installation des dépendances

### 1. Symfony

```bash
  composer install
```

### 2. Javascript

```bash
  # Avec npm
  npm install
  # Avec yarn
  yarn
```

### 3. Compiler les Assets

```bash
  # Avec npm
  npm run build
  npm run watch
  # Avec yarn
  yarn build
  yarn watch
```

## Création de la base de données

Pour créer la base de données, il faut au préalable démarrer le serveur MySql si il ne l'est pas.

> 💡<b>INFO :</b>
> Le mot clef `symfony console` peut être remplacé par `php bin/console` si vous n'utilisez pas le CLI de Symfony.


```bash
symfony console doctrine:database:create
symfony console doctrine:migrations:migrate
```

<!-- ### Charger des datas en base de données

```bash
symfony console doctrine:fixtures:load -n
``` -->

## Lancer l'application

Pour démarrer l'application

```bash
  symfony serve:start -d
```

## Explications du sujet

> Notre client, une grande marque de salles de sport, veut gérer les droits d'accès et de permissions d'une app web pour ses clients
franchisés qui possèdent des salles de sport.
> Chaque franchise (PARTENAIRE) a son propre contrat qui dépend de la somme qu’elle verse au client. Plus ou moins de permissions lui seront alors accessibles.

> Chaque PARTENAIRE (franchise) peut posséder plusieurs STRUCTURES (clubs de gym), et leur donne par défaut un nombre de permissions (outil de planning, newsletters, SMS, etc...) en fonction du contrat qu'il aura souscrit avec la marque.

> Chaque STRUCTURE (club de gym) est rattachée à un partenaire, et elle peut choisir d'activer ou non les permissions données par défaut par le contrat du partenaire.

> Les Partenaires et Structures ont un accès en LECTURE SEULE à leurs informations.
> Pour toute modification sur leurs permissions ou informations, ils doivent contacter l'administrateur STUDI FITNESS qui est le seul à avoir les pleins pouvoirs.
