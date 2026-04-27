# SILENT-GUARD

Bienvenue sur le README de mon projet.  
Ce document présente le fonctionnement, les branchements et l’utilisation de mon système d’alarme silencieuse.


# SOMMAIRE

- Matériel  
- Configuration  
- Branchements  
- Scripts  
- Fonctionnement  
- Explication du code  


# MATERIEL

Pour réaliser ce projet, j’ai utilisé :

- une carte UCA (RFThings)  
- un capteur PIR (détection de mouvement)  
- un écran OLED  
- un bouton poussoir  
- une LED  
- des fils de connexion  


# LA CONFIGURATION

1. Télécharger Arduino IDE (version 1.6.8 minimum)  
2. Brancher la carte UCA à l’ordinateur  
3. Vérifier que la carte est bien détectée (port COM3 par exemple)  


# LES BRANCHEMENTS

## Écran OLED

⚠️ IMPORTANT : débrancher la carte avant de faire les branchements

- GND → GND  
- VCC → 5V  
- D0 → D13  
- D1 → D11  
- RES → D8  
- DC → D9  
- CS → D10  


## Capteur PIR

- GND → GND  
- VCC → 3V  
- OUT → A3  


# LES SCRIPTS

## Arduino

Le code Arduino permet de gérer les différents composants du projet.

Il permet notamment :
- de lire les données du capteur PIR  
- de détecter une présence  
- de gérer le bouton  
- d’afficher les informations sur l’écran OLED  
- de déclencher une alerte  

---

## Python

Un script Python est utilisé pour envoyer un email en cas d’intrusion.

Installation :


Exécution :



Il suffit de modifier les adresses email dans le script pour recevoir les notifications.

---

# FONCTIONNEMENT

Le système fonctionne de la manière suivante :

- Le capteur PIR détecte un mouvement  
- La carte UCA reçoit et traite l’information  
- Une alerte est déclenchée (LED + écran OLED)  
- Un message peut être envoyé en cas d’intrusion  

Pour désactiver l’alarme :

- appuyer 2 fois sur le bouton  
- puis rester appuyé pendant 3 secondes  

Après plusieurs erreurs :

- le système détecte une tentative d’intrusion  
- une alerte est envoyée  

---

# EXPLICATION DU CODE

## Partie Arduino

Le programme Arduino est composé de plusieurs parties :

- initialisation des composants  
- lecture du capteur PIR  
- gestion du bouton  
- affichage sur écran OLED  
- détection des erreurs et alertes  

---

## Partie Python

Le script Python permet :

- de lire les données envoyées par la carte via le port série  
- d’envoyer automatiquement un email  
- de gérer les erreurs de connexion  

---

# CONCLUSION

Ce projet permet de créer une alarme silencieuse simple et efficace.

Il montre comment utiliser un capteur, une carte électronique et un système de communication pour détecter une intrusion et envoyer une alerte.

Une amélioration possible serait d’ajouter une communication sans fil (LoRa) pour rendre le système totalement autonome.

---

# AUTEUR

Projet réalisé par Rethik Palani dans le cadre du module Communication Sans Fil.
