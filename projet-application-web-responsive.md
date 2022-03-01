## MariaDB

Installer [MariaDB](https://mariadb.org/download/) (de préférence, la version LTS actuelle).

### HeidiSQL

Par défaut, MariaDB est livré avec l'éditeur HeidiSQL.

#### Créer une base de données

Dans le panneau de gauche, sélectionnez l'élément racine puis faites un clic droit n'importe où dans le panneau et choisissez l'option `Créer un(e) nouveau(el/elle) -> Base de données`.

#### Supprimer une base de données

Dans le panneau de gauche, faites un clic droit sur la base de données à supprimer puis choisissez l'option `Retirer (DROP)...`.

#### Editer une base de données

Dans le panneau de gauche, faites un clic droit sur la base de données à supprimer puis choisissez l'option `Edition`.

#### Créer une table

Dans le panneau de gauche, faites un clic droit sur la base de données concernée et choisissez l'option `Créer un(e) nouveau(el/elle) -> Table`.

Dans le panneau de droite, saisissez un nom pour la table et cliquez sur le bouton `Ajouter` pour ajouter une colonne.

Configurez les colonnes dans la partie basse du panneau puis validez la création en cliquant sur le bouton `Enregistrer`.

#### Supprimer une table

Dans le panneau de gauche, faites un clic droit sur la table à supprimer et choisissez l'option `Retirer (DROP)...`.

#### Editer une table

Dans le panneau de gauche, faites un clic droit sur la table à éditer puis choisissez l'option `Edition`.

## NodeJS

Installez [NodeJS](https://nodejs.org/) (de préférence la version LTS).

### Créer un projet

Créez un répertoire et ouvrez le avec VS Code.

Ouvrez une fenêtre de terminal et saisissez la commande `node init -y`.

```
node init -y
```

**Remarque :** L'option `-y` permet de créer un fichier `package.json` sans avoir à saisir d'informations.

### Importer le connecteur MariaDB

Dans une fenêtre de terminal, saisissez la commande `$ npm install mariadb`.

```
$ npm install mariadb
```

```js
const mariadb = require("mariadb");

const pool = mariadb.createPool({
  host: "localhost",
  user: "root",
  password: "root",
  connectionLimit: 5,
});

async function asyncFunction() {
  let conn;
  try {
    conn = await pool.getConnection();
    const rows = await conn.query("SELECT 1 as val");
    console.log(rows); //[ {val: 1}, meta: ... ]
    const res = await conn.query("INSERT INTO myTable value (?, ?)", [
      1,
      "mariadb",
    ]);
    console.log(res); // { affectedRows: 1, insertId: 1, warningStatus: 0 }
  } catch (err) {
    throw err;
  } finally {
    if (conn) return conn.end();
  }
}
```

### CRUD

```
INSERT INTO nom_table (nom_colonne1, nom_colonne2) VALUES (valeur1, valeur2);
SELECT * FROM nom_table;
UPDATE nom_table SET nom_colonne = valeur WHERE condition;
DELETE nom_table WHERE condition;
```

## Express

```
npm install express
```

```js
const express = require("express");
const app = express();
```
