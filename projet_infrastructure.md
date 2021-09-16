# Projet Infrastructure

## Installation d'une machine virtuelle

### VirtualBox

#### Installation

Allez sur le site de [VirtualBox](https://www.virtualbox.org/).

Sur la page d'accueil, cliquez sur le bouton `Download VirtualBox X.X`.

![page d'accueil de VirtualBox](images/S6iiFo9nRL.png)

Téléchargez et installez VirtualBox pour Windows (ne fermez pas la fenêtre du navigateur).

![Lien vers VirtualBox pour Windows](images/xYVh0QU67d.png)

Faites défiler la page précédente, téléchargez et installez `VirtualBox X.X.XX Oracle VM VirtualBox Extension Pack`.

![Lien vers VirtualBox 6.1.26 Oracle VM VirtualBox Extension Pack](images/cS30n5iX8u.png)

#### Configuration

Exécutez VirtualBox.

Cliquez sur le menu `Machine -> Nouvelle…` (`CTRL+N`).

Dans la boîte de dialogue `Nom et système d'exploitation`, donnez un nom à la nouvelle machine virtuelle (exemple : `debian`), sélectionnez un répertoire de destination, choisissez le type `Linux` et la version `Debian (64-bit)` puis cliquez sur le bouton `Suivant`.

![boîte de dialogue Nom et système d'exploitation](images/J4tQbfanDE.png)

Dans la boîte de dialogue `Taille de la mémoire`, sélectionnez si possible `2048` en RAM puis cliquez sur le bouton `Suivant`.

![boîte de dialogue Taille de la mémoire](images/kBIrk0eu0L.png)

Dans la boîte de dialogue `Disque dur`, sélectionnez l'option par défaut `Créer un disque dur virtuel maintenant` puis cliquez sur le bouton `Suivant`.

![boîte de dialogue Disque dur](images/0dEbxaPYV6.png)

Dans la boîte de dialogue `Type de fichier de disque dur`, sélectionnez l'option par défaut `VDI (VirtualBox Disk Image)` puis cliquez sur le bouton `Suivant`.

![boîte de dialogue Type de fichier de disque dur](images/8VJEG8GdRp.png)

Dans la boîte de dialogue `Stockage sur disque dur physique`, sélectionnez l'option par défaut `Dynamiquement alloué` puis cliquez sur le bouton `Suivant`.

![boîte de dialogue Stockage sur disque dur physique](images/gNhbXkCdOb.png)

Dans la boîte de dialogue `Emplacement du fichier et taille`, laissez le chemin par défaut mais saisissez si possible `20,00` Go en taille du disque virtuel puis cliquez sur le bouton `Créer`.

![boîte de dialogue Emplacement du fichier et taille](images/3nBMEo6oBR.png)

Une nouvelle machine virtuelle apparaît sur l'écran principal de VirtualBox. Sélectionnez cette machine virtuelle et cliquez sur le bouton `Configuration`.

![Ecran principal de VirtualBox et bouton Configuration](images/3Y7d9MlsGx.png)

Dans la section `Système`, onglet `Processeur`, saisissez `2` dans le champ `Nombre de processeurs` et cochez dans les `Fonctions avancées` les options `Activer PAE/NX` et `Activer VT-x/ADM-Vimbriqué` (si disponible).

![Configuration, section Système, onglet Processeur](images/Dl3cWJysSO.png)

Dans la section `Réseau`, onglet `Adapter1`, sélectionnez l'option `Accès par pont` dans le `Mode d'accès réseau`. Cliquez ensuite sur le bouton `OK`.

**Remarque :** L'option `Accès par pont` ne marche pas sur le réseau du CESI.

![Configuration, section Réseau, onglet Adapter1](images/GeF1kLE2dP.png)

#### Téléchargement d'une image Debian

Récupérez l'image de la dernière version de la distribution Debian sur le site [debian.org](https://www.debian.org/).

![Site debian.org](images/Hi1KvZBDyE.png)

#### Sélection de l'image Debian

Dans la section `Stockage`, sur l'option `Controller IDE`, cliquez sur l'icône `Ajoute un lecteur optique.`.

![Configuration, section Réseau, onglet Adapter1](images/DABwAFjRGA.png)

Dans la boîte de dialogue `nom_machine_virtuelle - Optical Disk Selector`, cliquez sur le bouton `Ajouter`.

![boîte de dialogue nom_machine_virtuelle - Optical Disk Selector](images/VkpLaQqFAb.png)

Dans la boîte de dialogue `Choisissez un fichier de disque optique virtuel`, parcourez votre ordinateur et sélectionnez l'image de Debian puis cliquez sur le bouton `Ouvrir`.

![boîte de dialogue Choisissez un fichier de disque optique virtuel](images/h6L1g24gWI.png)

Dans la boîte de dialogue `nom_machine_virtuelle - Optical Disk Selector`, sélectionnez l'image disque de Debian et cliquez sur le bouton `Choisir`.

Fermez la boite de dialogue `Paramètres` en cliquant sur le bouton `OK`.

#### Installation de Debian

Sur l'écran principal de VirtualBox, sélectionnez la machine virtuelle et cliquez sur le bouton `Démarrer`.

Lors de l'installation de Debian, utilisez les flèches du clavier pour effectuer une sélection, la touche `ESPACE` pour cocher une option et la touche `ENTREE` pour valider.

Sélectionnez l'option `Install`.

**Très important !** Sélectionnez l'option `Install` et surtout pas l'option `Graphical Install`.

![option install](images/lLTwVS3Nxo.png)

Sélectionnez la langue utilisée lors de l'installation et validez.

**Remarque :** Il est préférable d'utiliser l'anglais pour faciliter la recherche lors de l'apparition de messages d'erreur.

![option langue de l'installation](images/EFzyd1ucqt.png)

Sélectionnez la time zone `United States`.

**Remarque :** Si vous ne trouvez pas le français, sélectionnez l'option `Other`, puis `Europe`, puis `France`. Cependant, un problème va se produire par la suite car le language anglais et la time zone française ne sont pas compatible.

![option time zone](images/YhbvHyUB5Z.png)

Sélectionnez le type de clavier `French`.

![option du clavier](images/Xll4WdA0kH.png)

Saisissez le nom de la machine virtuelle.

![option nom](images/I2a8lPEypk.png)

Saisissez le nom de domaine de la machine virtuelle.

![option nom de domaine](images/y5f5Bhrsen.png)

Saisissez le mot de passe du compte *root*.

**Attention !** Le compte *root* est l'administrateur principal de la machine. Il est très important de sécuriser ce mot de passe.

![option mot de passe root](images/v6oQ2A00IZ.png)

Saisissez à nouveau le mot de passe du compte *root*.

**Remarque :** Vous pouvez afficher les mots de passe en clair si vous cochez la case `Show Password in Clear`.

![option confirmation du mot de passe root](images/AuOWpA6paa.png)

Saisissez le nom complet du premier compte utilisateur.

![option nom complet de compte utilisateur](images/1KPAwe8ZJS.png)

Saisissez l'identifiant du premier compte utilisateur.

![option identifiant de compte utilisateur](images/mH75Bz04KY.png)

Saisissez le mot de passe du compte utilisateur.

![option mot de passe compte utilisateur](images/8d5e17FBiu.png)

Saisissez à nouveau le mot de passe du compte utilisateur.

![option confirmation du mot de passe compte utilisateur](images/VjWPnm4k47.png)

Sélectionnez la time zone de la machine (le choix n'est pas important et pourra être modifié par la suite).

![option time zone](images/6ZaelYh7kW.png)

Sélectionnez l'option `Guided - use entire disk` pour partitionner et utiliser l'intégralité de l'espace disque réservé lors de la configuration de la machine virtuelle.

![option partition de disques](images/wlMDh4TJUN.png)

Vérifiez que le disque sélectionné est bien le bon.

![option sélection du disque à partitionner](images/6aMdRHj2ZM.png)

Sélectionnez l'option de partitionnement `All files in one partition (recommended for new users)`.

![option de partitionnement](images/lnlYleVuDu.png)



![](images/E77Apuzy0h.png)

![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)
![](images/.png)

### Apache



### MariaDB



### PHP



#### PHPMyAdmin



### Wordpress

#### Installation

Positionnez-vous dans le dossier `/var/www/` :

```
sudo cd /var/www
```

Téléchargez l'archive de Worpress :

```
sudo wget https://wordpress.org/latest.tar.gz
```

Décompressez l'archive :

```
sudo tar -xzvf latest.tar.gz
```

Le dossier `wordpress` conrrespond à la racine du site Wordpress.

Supprimez l'archive devenue inutile.

```
sudo rm latest.tar.gz
```

#### Configuration d'un vhost associé à Wordpress

------------

#### Configuration de Wordpress

Vous pouvez accéder au site Wordpress depuis une machine cliente si vous utilisez l'adresse IP de la machine virtuelle dans le navigateur.

```
XXX.XXX.XXX.XXX
```

Il vaut mieux toutefois configurer le fichier `hosts` de la machine cliente pour accéder au site en utilisant un nom de domaine.

##### Association du nom de domaine à la machine virtuelle sur le client

Vous devez éditer le fichier `hosts` de votre machine cliente pour associer l'adresse IP de la machine virtuelle où est hébergée le serveur web et le nom de domaine.

Sur Windows, ce fichier `hosts` se situe à l'emplacement `C:\Windows\System32\drivers\etc\`.

**Attention !** Avant de l'ouvrir avec un éditeur de texte, vous devez modifier les droits associés à ce fichier.

Faites un clic droit sur le fichier `hosts` et sélectionnez l'option `Propriétés`.

Cliquez sur le bouton `Modifier...` dans la boite de dialogue `Propriétés de : hosts`.

![boite de dialogue Propriétés de : hosts](images/a5hn1uQJjO.png)

Sélectionnez `Utilisateurs (nom_machine\Utilisateurs)` dans la section `Noms de groupes ou d'utilisateurs` et cochez la case `Contrôle total, Autoriser` dans la section `Autorisations pour Utilisateurs` puis cliquez sur le bouton `OK`.

![boite de dialogue Autorisations pour hosts](images/1uiZcKft99.png)

Sur Linux, ce fichier `hosts` se situe à l'emplacement `/etc/`.

Ouvrez le fichier `hosts` avec un éditeur de texte. Ajoutez une ligne avec l'adresse IP du serveur Linux suivie du nom de domaine.

```
XXX.XXX.XXX.XXX domaine.com
```

![fichier hosts édité](images/aWsLRLB5OM.png)

##### Configuration de Wordpress

Ouvrez le navigateur et accédez au domaine associé au chemin vers Wordpress sur le serveur web :

```

```





Accéder à une machine en SSH

```
ssh -p numero_port identifiant@adresse_machine
```

![commande ssh](images/jLkZc8YXD0.png)





Déployer une machine virtuelle Linux Server (distribution de votre choix).
Vous utiliserez une version Linux sans interface graphique. Cela permet de diminuer la surface 
d’attaque, certaines options ne sont accessibles qu’en ligne de commande et cela permet également 
d’optimiser l’utilisation des ressources (affichage gourmand).
INFO : La réalisation de ce TP sur Windows Server est envisageable, mais vous serez limité dans 
certaines actions et bridés sur certains paramétrages.
Il faudra créer un utilisateur « cesi » avec le mot de passe de votre choix.

## Installation et configuration des outils

- Lancer le serveur et se connecter.
- Créer un utilisateur « cesi » si ce n’est pas déjà fait.
- Nommer la machine
- Mettre une IP fixe sur le serveur.
- Installer les outils suivants : 
  - Apache
  - PHP version 7 (php7.x)
  - Une base de données relationnelles
✓ Attention à bien noter le mot de passe root
  - Modules PHP nécessaires
- Démarrer Apache et s’assurer que le service démarre systématiquement en même temps 
que la machine
- Tester depuis la machine hôte (votre PC) si le serveur Apache (de la machine virtuelle) 
répond correctement (en tapant l’adresse IP du serveur web)
  - Cela devrait afficher un message par défaut (de votre distribution) qui prouve le bon 
fonctionnement
- Tester si PHP est bien fonctionnel également
  - Créer un fichier info.php dans le répertoire www/html et y ajouter :
<?php
phpinfo();
?>
  - Afficher ensuite depuis le navigateur de votre machine hôte le fichier. Ce qui 
affichera la configuration de votre serveur web
✓ Vous devriez avoir ça (voir Annexe 1 – résultat du fichier info.php)
Si tout est ok, cette partie est terminée !
Faites un screenshot du navigateur web. Veillez à stipuler dans le nom du fichier le 
numéro de la partie validée.
Projet : Système / Base de données / Scripting - V2 - 14/10/2019 CESI
5

## Partie 3 : Premier site

Une fois Apache et PHP bien fonctionnels, vous pouvez créer une première page web.
INFO : Vous aurez pris le soin d’affecter une IP fixe sur votre VM, ce qui simplifiera les différents tests, 
vous pouvez même créer un alias dans le fichier hosts de la machine hôte.
Se rendre dans le dossier www du serveur web (VM) :
- Créer un nouveau dossier « monsite » à la racine 
- Créer un fichier « index.php » dans ce nouveau dossier 
- Ajouter du code PHP dans le fichier (une commande echo par exemple) 
- Essayer d’atteindre le site depuis sa machine hôte

## Partie 4 : Accès au site & sécurisation

Sécurité 
- Installer SSH1
si nécessaire
- Configurer SSH si besoin
- S’assurer qu’il est bien possible de se connecter en SSH depuis une autre machine2
➢ Vous devez générer une authentification par certificat si ce n’est pas déjà fait
- Mise en place d’un mécanisme de sécurité pour éviter les attaques brutes forces (de mot de 
passe)
- Configurer le pare-feu en adéquation avec votre stratégie (règles / ports)
INFO : Il devra être possible d’ajouter à tout moment un nouvel utilisateur « distant » pouvant se 
connecter en SSH avec son compte.
Client FTP 
Tester depuis la machine hôte de se connecter avec un client FTP (exemple : WinSCP)
➢ Créer 2 utilisateurs virtuels « Dev1 » et « Dev2 » qui pourront interagir avec le serveur web
• Chaque utilisateur (développeur) aura un répertoire virtuel
• Chaque utilisateur accédera par défaut au répertoire « monsite » et ne pourra pas en 
sortir (jail)
• Les utilisateurs ne peuvent pas modifier les fichiers « systèmes »
➢ Se connecter en SFTP avec chaque utilisateur (tester)
➢ Modifier le fichier par défaut du site
Tester en affichant la page web « modifiée » dans le navigateur.
1 Utiliser la version libre - Documentation d’OpenSSH sur internet
2 Depuis sa machine hôte
Projet : Système / Base de données / Scripting - V2 - 14/10/2019 CESI
6

## Partie 5 : Configuration de la base de données

Se connecter à la base de données
Exemple :
mysql -u root -p
Créer une base de données, vous pourrez la nommer cesibdd
➢ Cette base de données sera utile pour déployer un site (CMS) dans la suite de ce projet
Créer un nouvel utilisateur « dibdd » et attribuez-lui les privilèges maximum sur cette nouvelle base 
de données
➢ Ce nouvel utilisateur sera utilisé pour se connecter à la base et accéder aux données dans la 
suite de ce projet

## Partie 6 : Installation d’un nouveau site

1. Téléchargement, installation & configuration 
- Télécharger sur votre serveur la dernière version du CMS.
- Placer le CMS dans le répertoire de destination.
➢ Vous devrez le placer directement dans le répertoire www d’Apache
➢ Veillez à bien conserver votre premier dossier monsite (du dossier www)
- Installer le CMS
➢ En cas de difficulté, pensez à lire le fichier README.txt à la racine du projet (CMS)
- Créer un nouveau vhost pointant sur le dossier
- Se connecter en administrateur sur le CMS nouvellement installé
2. Modification CMS 
- Modifier la page d’accueil de votre site
- Ajouter un ou deux contenus
- Personnaliser le site comme bon vous semble
Dans cette partie nous allons vous demander d’installer un nouveau site reposant sur un CMS 
(Wordpress ou Drupal) sur votre serveur actuel.
Projet : Système / Base de données / Scripting - V2 - 14/10/2019 CESI
7

## Partie 7 : Serveur de Pré-Prod / Serveur de Production

Idéalement, vous serez dans la même configuration. Si ce n’est pas le cas, n’hésitez pas à dupliquer 
(cloner) le serveur3
le plus abouti / fonctionnel des deux.
✓ Serveur A = Serveur de pré-production
✓ Serveur B = Serveur de production
Test 
- Dans un premier temps essayez de pinger le serveur A depuis le serveur B avec leur nom (et 
non pas leur adresse IP)
- Essayez ensuite d’afficher le site depuis un navigateur du même réseau
- Connectez-vous en SSH sur le serveur de développement (Serveur A)
A ce stade, vous devriez avoir quelques contenus sur votre serveur A (Cf. chapitre précédent –
Modification CMS). Si ce n’est pas le cas, merci de vous y reporter avant de passer à la suite.
Préparation à la migration du site 
1. Faire une extraction de la base de données (dump SQL) dans son état actuel
2. Connectez-vous en SFTP sur le serveur
3. Récupérer la base de données « dumpée »
4. Récupérer si nécessaire l’archive des dossiers « personnalisé » de votre CMS
➢ Ici, nous parlons des dossiers et fichiers qui ont pu être ajouté ou qui aurait pu évoluer
depuis l’installation du CMS
➢ Lire la documentation du CMS ou suivre un article / tuto expliquant comment migrer / 
déployer le site
Serveur de production 
Entre le serveur A et le serveur B
1. Récupérer les sources (dossiers du site CMS sauvegardés) du serveur A et les copier sur le 
serveur B
2. Importer la BDD « dumpées » du serveur A vers le serveur B
3. Modifier les éventuels fichiers de configuration natifs du CMS de manière à ce que le site soit 
opérationnel sur le serveur B.
➢ Lire la documentation officielle du CMS
➢ Suivre un article / tuto au sujet de la migration / déploiement du CMS concerné
4. Depuis la machine hôte ou depuis le serveur A, tester le bon fonctionnement et affichage du 
site nouvellement déployé sur le serveur B.
3 Le serveur ici est très certainement une machine virtuelle sur votre machine hôte.
Pour réaliser cette partie, il est conseillé d’être à deux (avec votre binôme). L’un jouera le 
rôle du serveur pré-prod, l’autre le rôle du serveur de production. Vous pourrez changer 
les rôles afin d’aborder chacun les objectifs
Ici, nous allons migrer (en prod) le site du serveur A vers le serveur B.
Projet : Système / Base de données / Scripting - V2 - 14/10/2019 CESI
8

## Partie 8 : Automatisation

Créer un script qui permet : 
• Lorsque l’on va créer un nouvel utilisateur son site web portant son nom sera créé.
• Le répertoire par défaut de l’utilisateur sera /home/<UTILISATEUR>/public_html
• Créer un répertoire logs par utilisateur
• Stocker l’horodatage de la création du compte dans un fichier
Création d’un nouvel utilisateur 
▪ Créer un nouvel utilisateur « cesien » (ce sera votre profil pour le développement)
▪ Assurez-vous que l’on puisse accéder à la page web4 de l’utilisateur via son nom
Il vous sera demandé de faire une démonstration lors de la correction.
Sauvegarde / backup 
Créer une tâche planifiée (script) permettant d’automatiser la sauvegarde quotidienne de la base de 
données du site du serveur de production.

## Partie 9 : Sécurisation du site et disponibilité

HTTPS 
▪ Activer le module SSL dans Apache
INFO : Par défaut, si vous activez seulement le mod_ssl et que vous relancez les services 
Apache, vous avez un certificat « Self-Signed ». Le navigateur ne considère pas ce genre de 
certificat comme « fiable », ce qui a pour effet d’alerter le visiteur de votre site (avec un 
message demandant s’il fait confiance au site afin d’y accéder).
Conf Apache 
▪ Mettre en place l’url rewriting sur votre projet
o Ajouter le « www » dans l’url du site
o Rediriger l’url http://VOTRE_URL vers https://VOTRE_URL
▪ Créer des redirections vers des pages d’erreurs en fonction du code d’erreur
o Erreurs : 401, 403, 404, 500
o Un concours de la plus belle « page 404 » sera organisé ! ☺
4
 Une page web ou un site web – un fichier index.php avec une instruction echo à l’intérieur suffit pour tester
Dans cette partie nous allons vous demander de réaliser quelques opérations pour sécuriser votre 
site. Vous pourrez appliquer cela sur le dossier public_html de l’utilisateur cesien ou sur le projet 
« monsite » du répertoire www.
Projet : Système / Base de données / Scripting - V2 - 14/10/2019 CESI
9

## Partie 10 : Disponibilité du site – Bonus

Cache 
Mettre en place un système de cache sur l’un de vos projets (exemple : memcache)
Load Balancing 
La répartition de charge (= load balancing en anglais, littéralement équilibrage de charge) est une 
technique utilisée en informatique pour distribuer un travail entre plusieurs serveurs.
Les avantages sont nombreux 
▪ Augmentation de la qualité des services
▪ Amélioration des temps de réponse des services
▪ Capacité à pallier la défaillance d'une ou de plusieurs machines
▪ Possibilité d'ajouter des serveurs sans interruption de service
Mise en place 
Mettre en place un système de Load Balancing sur l’instance de votre serveur. L’outil haproxy
permet d’atteindre ces objectifs.
Cf. Annexe 2 – Schéma simplifié d’un système de Load Balancing
Vous pouvez vous informer ici : https://linuxfr.org/forums/linux-general/posts/tuto-howto-ubuntu￾debian-load-balancing-redirection-vers-plusieurs-vhost-avec-haproxy







Connaitre son IP sur Windows
Commande ipconfig
Carte réseau sans fil Wi-Fi :
    ...
   Adresse IPv4. . . . . . . . . . . . . .: XXX.XXX.XXX.XXX

Connaître son IP sur Linux
Commande hostname -I

Nom de domaine pour notre projet : group2.local

Créer une IP statique
Vérifier que le paquet ifupdown est installé.
ifup
S'il n'est pas installé :
sudo apt-get install ifupdown


Vider le cache DNS de windows
ipconfig /flushdns

Configuration du fichier hosts
La machine qui souhaite consulter le site sur le serveur web doit configurer son fichier hosts pour associer le nom de domaine avec l'adresse IP du serveur.
192.168.10.10 domaine.com

Sur Windows, le fichier hosts se trouve à l'emplacement C:/windows/system32/drivers/etc.
Sur Linux, le fichier hosts se trouve à l'emplacement /etc/.

Sur le serveur, le fichier hosts doit également être configuré car le serveur web peut proposer plusieurs noms de domaines. Il faut associer le nom de domaine avec l'adresse IP 127.0.0.1.
127.0.0.1 localhost domaine.com

Savoir si un service est lancé au démarrage
service --status-all
Un service avec + indique qu'il est démarré.
Un service avec - indique qu'il est arrêté.
Si le service apache2 est démarré, le critère est validé.

