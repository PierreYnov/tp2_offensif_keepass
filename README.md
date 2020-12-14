# TP2 : Attaques sur les mots de passe
## Mise en oeuvre et utilisation d'un gestionnaire de mots de passe

## Classe : B3B
## Elèves : Emma Durand **[@emmadrd912](https://github.com/emmadrd912)** et Pierre Ceberio **[@PierreYnov](https://github.com/PierreYnov)** 

![](https://cdnx.nextinpact.com/data-next/images/bd/wide-linked-media/799.jpg)

# Sommaire 

- [Le Lab](#le-lab)
- [Découverte de l'outil](#d%C3%A9couverte-de-loutil)
- [Configuration et utilisation du gestionnaire de mot de passe](#configuration-et-utilisation-du-gestionnaire-de-mot-de-passe)
    - [I. Étapes préliminaires](#i-%C3%A9tapes-pr%C3%A9liminaires)
    - [II. Utilisation de l'outil](#ii-utilisation-de-loutil)
- [Fonctionnalités annexes du gestionnaire de mot de passe ](#fonctionnalit%C3%A9s-annexes-du-gestionnaire-de-mot-de-passe)
    - [I. Générateur de mots de passe](#i-g%C3%A9n%C3%A9rateur-de-mots-de-passe)
    - [II. Tâches automatisées](#ii-t%C3%A2ches-automatis%C3%A9es)
- [Sécurisation de la solution](#s%C3%A9curisation-de-la-solution)

## Le Lab

Logiciel [Keepass](https://keepass.info/)

## Découverte de l'outil

**Sous quelle forme sont stocke les mdp enregistre dans le logiciel ?**

- Les mots de passe sont stockés dans une base de données.

**Quel algo sont utilise pour cela ?**

- AES/Rijndael, ChaCha20 (and with plugins: Twofish, Serpent, GOST, ...)


**Pourquoi l'anssi recommande la version 2.41 plutot que la 1.36 ?**

C'est une version plus stable, des vulnéraibilités ont été corrigées, dont une attaque par [MITM](https://www.cert.ssi.gouv.fr/actualite/CERTFR-2016-ACT-023/). Les hashes et les signatures pour le contrôle d’intégrité sont disponibles, et les binaires du programme sont signés numériquement (Authenticode). 

## Configuration et utilisation du gestionnaire de mot de passe 

### I. Étapes préliminaires 


    créez un compte user sur votre poste : mdp fort + membre groupe admin

    ouvrir keepass et renseigner un master password d'au moins 15 caractere (grace à  Méthode des premières lettres ou méthode phonétique.)


Je crée une nouvelle base de donnée :

![](https://i.gyazo.com/6299233dcd6bf48b27a4db34e9417ead.png)

Il m'est demandé de renseinger le Master Password :

![](https://i.gyazo.com/8c6cc5aab3254482a4b3f8e567ed240f.png)

J'utilise la méthode phonétique pour avoir un mot de passe fort que je puisse retenir, ici ma phrase est :

``C’est un fameux trois-mâts, Hisse et ho et J'ai acheté huit CD pour cent euros cet après-midi``

Ce qui me donne comme mot de passe :

``c1famE3ma,is&o&ght8CD%E7am``

### II. Utilisation de l'outil 


Je crée le compte admin dans la section Windows :

![](https://i.gyazo.com/fbc0de4585bfd6bc0643050f27c11e53.png)

Je renseigne les informations puis sauvegarde

![](https://i.gyazo.com/1df843b8397f1737060174bd25d784a4.png)

Je fais pareil dans la section mail pour mon compte Ynov.


Je me connecte au SSO de Ynov en copier-coller :

![](img/copier-coller.gif)

Je me connecte au SSO de Ynov en auto-type :

![](img/autotype.gif)

## Fonctionnalités annexes du gestionnaire de mot de passe 
### I. Générateur de mots de passe 

    generer un new master password de la db en utilisant le generateur, avec les contrainte de complexité plus haut

J'utilise le générateur pour générer un nouveau Master Password, avec 15 caractères minimum :

![](https://i.gyazo.com/a612df422dedf767efcf9a34a8285aa5.png)

Voici le nouveau mot de passe : @:j1/oFt3lGjF;3


![](https://i.gyazo.com/48f9124d05f06dbce8c7f9c62ad87fc0.png)

### II. Tâches automatisées 

**Expliquer la fonctionnalite Triggers**
 
La fonction trigger permet de sauvegarder une base de donées et de l'enreistrer dans un deuxième endroit.

On va dans Add Trigger

![](https://i.gyazo.com/4aa46b9bf623e1b15e6abcf858f687e5.png)

    créer un trigger pour save auto la base à la fermeture, il ne doit conserver que les 3 dernier exemplaire dans son historique

## Sécurisation de la solution

    faite 2 mesure de sécurité : imprimer une feuille d'urgence avec le master password

    créer un script robocopy pour save la db
