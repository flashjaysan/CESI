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

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

![](images/E77Apuzy0h.png)

## Configuration de Debian

### Notions de base

Sur Linux, la plupart des actions se font en ligne de commande. Certains outils ont une gestion automatisée via une interface graphique mais la plupart ne possèdent que des options en ligne de commande.

Une commande commence par le nom du programme/de la commande suivi de ses options. Il faut valider chaque commande  avec la touche ENTRÉE.

Chaque commande possède un manuel (généralement accessible en ligne) pour connaître les options qu'elle propose mais généralement, les débutants préfèrent chercher sur Internet car le manuel est souvent difficile d'accès.

### L'éditeur de texte Nano

La commande `nano` suivie d'un chemin de fichier demande d'ouvrir ce fichier dans un éditeur de texte appelé Nano.

Les commandes de cet éditeur apparaissent au bas de l'écran.

**Attention !** Dans Nano, les commandes s'exécutent directement sans validation par la touche `ENTRÉE`.

- Pour quitter, appuyez sur `CTRL+X`.
- Pour sauvegarder le fichier édité, appuyez sur `CTRL+O`. Si le fichier existe déjà, son nom apparait en bas de la fenêtre pour vérification. Si c'est un nouveau fichier, vous devez saisir son nom. Validez si vous souhaitez vraiment sauvegarder vos modifications. Pour annuler la sauvegarde, appuyez sur `CTRL+O`.

### Mise à jour du système 

En premier lieu, assurez-vous avant tout que le système est bien à jour. Pour cela, on commence par préciser qu'on veut saisir des commandes en mode super utilisateur (su), l'équivalent du mode Administrateur.
Saisissez la commande suivante et validez :
su -

Remarque : Pensez bien à séparer la commande et le tiret avec un espace. L'espace sert de séparateur.

On utilise ensuite la commande apt-get qui permet d'installer, et de gérer la mise à jour de fonctionnalités sur le système. Ici on utilise l'opérateur && pour appeler plusieurs commandes à la suite.
L'option update met à jour les fonctionnalités déjà présentes.
L'option upgrade met à niveau (installe la dernière version) les fonctionnalités déjà présentes.
L'option dist-upgrade met à jour le système (la distribution Linux que vous avez installée).


Saisissez la commande suivante et validez :
apt-get update && apt-get upgrade && apt-get dist-upgrade

Synchronisation de l’horloge système

On s’assure que l’horloge système sera synchronisée grâce à ntp
apt-get install ntp ntpdate


La commande sudo

sudo est une commande qui permet aux utilisateurs d’exécuter des commandes administrateur de manière temporaire. Il faut d'abord l'installer.

Pour l’installer il convient tout d’abord de s’authentifier en tant que root (administrateur principal) sur la machine (si ce n'est pas déjà fait).
su -
Pour quitter le compte super utilisateur, saisissez la commande exit :
exit
On utilise ensuite la commande apt-get pour installer (option install) la commande sudo.

apt-get install sudo



La commande sudo n'est accessible qu'aux membres du groupe qui lui sont associés ainsi qu'au compte root. Il faut donc ajouter l’utilisateur créé lors de l’installation au groupe sudo pour qu'il puisse utiliser lui aussi cette commande.
usermod -aG sudo NOM_UTILISATEUR_CREE_A_L_INSTALLATION 








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

[A COMPLETER]

### Apache

[A REDIGER]

### MariaDB

[A REDIGER]

### PHP

[A REDIGER]

![](images/0K7LDMJQpv.png)

#### PHPMyAdmin

[A REDIGER]

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

[A REDIGER]

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
[A REDIGER]
```





Accéder à une machine en SSH

```
ssh -p numero_port identifiant@adresse_machine
```

![commande ssh](images/jLkZc8YXD0.png)












Connaitre son IP sur Windows

Commande `ipconfig`
```
Carte réseau sans fil Wi-Fi :
    ...
   Adresse IPv4. . . . . . . . . . . . . .: XXX.XXX.XXX.XXX
   ```

Connaître son IP sur Linux

Commande `hostname -I`

Nom de domaine pour notre projet : group2.local

Créer une IP statique

Vérifier que le paquet `ifupdown` est installé.

```
ifup
```

S'il n'est pas installé :

```
sudo apt-get install ifupdown
```

Vider le cache DNS de windows

```
ipconfig /flushdns
```

### Configuration du fichier hosts

La machine qui souhaite consulter le site sur le serveur web doit configurer son fichier hosts pour associer le nom de domaine avec l'adresse IP du serveur.
192.168.10.10 domaine.com

Sur Windows, le fichier hosts se trouve à l'emplacement C:/windows/system32/drivers/etc.
Sur Linux, le fichier hosts se trouve à l'emplacement /etc/.

Sur le serveur, le fichier hosts doit également être configuré car le serveur web peut proposer plusieurs noms de domaines. Il faut associer le nom de domaine avec l'adresse IP 127.0.0.1.
127.0.0.1 localhost domaine.com

### Savoir si un service est lancé au démarrage

Redémarrer la machine virtuelle puis saisir la commande suivante :

```
service --status-all
```

- Un service avec `+` indique qu'il est démarré.
- Un service avec `-` indique qu'il est arrêté.

![services](images/U0Hm8fkkGI.png)

Si le service apache2 est démarré, le critère est validé.

### Installer un clone d'image

Cliquez sur le bouton `Importer`.

![](images/4xF7iwdYH1.png)

![](images/kTEOieE6Zd.png)

![](images/Wuqa2vBv6g.png)

![](images/zux5l8Nyhy.png)

![](images/.png)

![](images/.png)

## Définir une adresse IP fixe sur un réseau

Connectez-vous au réseau.

Avant de définir l'adresse IP, vous devez trouver l'identifiant du périphérique reseau à utiliser. Utilisez la commande suivante et notez l'identifiant du périphérique.

```
ifconfig
```

![affichage commande ifconfig](images/uOLA7pJiFE.png)

Editez ensuite le fichier `interfaces` situé dans le dossier `/etc/network/`.

```
nano /etc/network/interfaces
```

Modifiez le fichier pour qu'il ressemble à l'image suivante et sauvegardez :

![fichier interfaces](images/RDLBsUO40z.png)

- Remplacez les zones pixellisées par l'identifiant de votre périphérique réseau.
- Remplacez l'adresse IP désirée à la place de celle encadrée.

Relancez les périphériques réseaux.

```
ifup identifiant_peripherique
```

Testez que la machine peut bien communiquer avec d'autres.

```
ping 1.1.1.1
```

Appuyez sur `CTRL+C` pour stopper le processus.






















