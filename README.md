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

gestionnaire de mdp pour limiter risque mauvaise utilisation mdp : Keepass


## Découverte de l'outil

sous quelle forme sont stocke les mdp enregistre dans le logiciel ?

Quel algo sont utilise pour cela ?


Pourquoi l'anssi recommande la version 2.41 plutot que la 1.36

dl la derniere version

## Configuration et utilisation du gestionnaire de mot de passe 

### I. Étapes préliminaires 


créez un compte user sur votre poste : mdp fort + membre groupe admin

ouvrir keepass et renseigner un master password d'au moins 15 caractere (grace à  Méthode des premières lettres ou méthode phonétique.)


### II. Utilisation de l'outil 

enregistrer le compte admin créé dans la section windows, il servir a demarrer une app avec elevation de privilege ( cmd.exe par exemple)

enregistrer le compte ynov dans la section email


se connecter sur les 2 compte d'apport en copier coller

puis en auto type

## Fonctionnalités annexes du gestionnaire de mot de passe 
### I. Générateur de mots de passe 

generer un new master password de la db en utilisant le generateur, avec les contrainte de complexité plus haut

### II. Tâches automatisées 

expliquer la fonctionnalite Triggers

créer un trigger pour save auto la base à la fermeture, il ne doit conserver que les 3 dernier exemplaire dans son historique

## Sécurisation de la solution

faite 2 mesure de sécurité : imprimer une feuille d'urgence avec le master password

créer un script robocopy pour save la db
