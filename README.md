# DATV-Easy © F1EJP
DATV broadcast from a PC on Windows for RADIO HAM

DATV-Easy is distributed under conditions: 

This software was developed for Amateur Radio experiments.
You have the freedom to distribute copies of this free software but its comercial use is not permitted.
This software uses libraries from the FFmpeg project media-autobuild_suite licensed under the GNU General Public License v3.0
Due to the non commercial nature of Amateur Radio there should be no problems in it's use only for Amateur Radio.

Version 1.0
- version initiale 25/11/2021

Version 1.15
- Ajout codec audio

Version 1.17- -
- Ajout relais hid

Version 1.20
- Curseur puissance

version 1.22
- Onglet nonitoring
- Ajout délai audio

Version 1.23
- Ajout Pluto sur Ethernet

Version 1.24
- Ajout codec AAC HE
- Ajout délai audio négatif

Version 1.25
- Première realase

Version 2.00
- ajout supervision derniers firmware de F5OEO
  testé sur 0201 0303 2103
- Ajout All automatic (image)
- Ajout commandes PTT relais manuel
- Extension des fréquences de 10 à 6000 MHz
- Ajout Fréquence par défaut de 15 fsp
- Commande de fréquence et SR par requête UDP pour utilisation avec les logiciel comme le longmynd client.

Version 2.03
- corrections réglage puissance plus progressif (log10)
- verrouillage menu Easy et QO100 en emission
- ajout possibilité réglage périodes tables dvb
- démarrage avec variation puissance sur firmware F5OEO
- graphisme dernier onglet
- correction commande par requete UDP

version 2.04
- correction parametres dvbt sur F5OEO
- correction bug memo sur param ini
- ajout IPudp server sur param .ini

version 2.05 > not good
- Correction save parametre F5OEO en emission (double start)
- Correction limite des 3 period
- choix des version F5OEO

version 2.06
- Correction bug choix des versions sur version précédentes
- Correction gain tx sur 0201
- corrections petits bugs choix modulation
- fourniture Driver Libiio v2.04

version 2.07
- ajout camera virtuelle d'OBS 
- ajout DroidCam pour le son mauvais pour la video car sort en 29.97 fsp
- ajout choix fréquences échantillonage du son 44100 et 48000
- ajout Réglage PCR / PTS en ms
- ajout Sécurité et alarme Température

version 2.08
- correction mémorisation period PCR PAT STD lors du décochage Automatic
- bug sur variable délai audio (coupure audio)
- ajout entrée audio par VB-Audio Cable
- Modification doc

version 2.09
- modification reset watchguard et nouveau programme ARDUINO (suite à quelques bug lors de l'enclenchement des relais)
- Ajout affichage fréquence rx QO100
- Ajout rolloff 0.15
- Choix mise au carré ou non des mesures de Watts dans fichier param.ini (suivant que la mesure est linéaire ou logarithmique)
- Modification "Automatic image" en "All automatic" pour audio également (mémorisation)
- Modification bouton PTT > reste enclenché indépendamment de Stop
- ajustage des seuils auto PCR
- reset AD9361 Pluto on exit
- application nouveaux paramètres par nouvel appui sur START +

version 2.10
- encore plus facile ! entrée audio et video sur camera Logitec C920 et C922 (pas besoin de conaître OBS ou Vmix)
- coche pour obtenir fenêtre de monitorage séparée
- diminution des seuils pour améliorer bas débit SR25 ou 20
- Ajout des nouvelles commandes à distance en UDP (voir fichier Remote UDP server)
- Bug sur commande DVBT du firmware 0303
- Ajout 4K

version 2.11
- dernière version fonctionelle ffmpeg 5.01
- optimisations parametrage ffmpeg pour bas débit et coupures:
	 reglage buffer, seuils talon data, valeurs automatiques

Version 2.12
- dernière version ffmpeg 2022 12 06 (plus récent que 5.1.2)
- ajout réglage temporisation sur etalonage LimeSDR mini (11 secondes par défaut)
- amélioration préréglages définition image
- ajout reglage GOP et B Frame dans fichier param.ini

Version 2.13
- suite nouvel ffmpeg amelioration codec aac et nouveaux bas débit en aac
- DVBT testé ok avec version firmware F5OEO 2202 et 2402 meilleurs en DVB-T
- bug sur fermeture formulaire monitoring
- Débit minimum réel en HE-AAC est de 16kb/s meilleurs résultat bas débit en AAC
- Ajout Audio SR à 16000 et bascule auto sur cette valeur pour faible débit
- Débit audio respecté permet de descendre réellement à 6 kb/s en aac pour faire très bas SR, 20, 25, 35 en QPSK !
	>> pour réception stable sur Minitiouner en SR 20 ou 25 passer Refresh timing à 300ms

Version 2.14
- Ajout coefficient gain maximum pour protéger amplis
- Ajout ancien paramètres pour carte NVIDIA non à jour "NVIDIA_old"
- Dernière version ffmpeg 22/01/2023 (12.2.0 Rev9)

version 2.15
- Choix  automatique du type de codec aac en fonction du débit
- Ajout Audio SR à 22050 et bascule auto sur cette valeur ou 16000 pour faible débit
- Débit minimum réel en HEv2-AAC est maintenant de 8kb/s meilleurs résultat bas débit reste 6kb/s en AAC
- A jout filtres passe-bas audio en fonction des SR
- Nouvel optimisation des paramètres automatiques
- Sur choix Pluto ajout reboot automatique à la sortie du logiciel
- Sur Start passage en mode DATV et sur Exit passage en mode passthrough
- Choix 5 IP possible sur Pluto

version 2.16
- Correctif bug mémorisation valeurs
- Amélioration timings relais et commande relais du Pluto sur USB
- Correction Bug sur ouvertures multiples fenetres Easy et Oscar100

version 2.17
- Passage sur ffmpeg version 6.0
- Ajout anciennes versions firmware F5OEO (ex 2908)
- Ajout Rolloff 0.10
- Ajout codec H266 VVC Expérimental seul le codage soft est disponible: surveillez charge CPU !
- fourniture dossier et .bat pour décodage h266 en udp
- Ajout visualisation vitesse encodage doit être > 99

version 2.18
- Ajout codec
- Compatibilité avec dernier firmware de F5OEO

version 3.00
- Passage sur ffmpeg 6.1.1
- derniere version VVenC 1.10
- modification choix codec entre codec hard et soft plus facile
- ajout commandes dernier firmware F5OEO 
- nouveau curseur réglage puissance par pas de 0.25dB
- ajout fec et gain automatique
- Ajout réglage GOP
- Ajout GSE
- Ajout codec AV1 en streaming sur GSE experimental démarrer vlc avant START
- Ajout réglage délai pour les relais

version 3.01
- separation et ajout fec gain automatique/manuel
- Modification sensibilité du curseur gain
- correction petits bugs

version 3.02
- correction petits bugs configuration
- ajustage seuils automatiques
- ajustage débit FecAuto
- ajout voyants sorties
- modification démarrage Pluto

version 3.03
- nouvelle compilation ffmpeg 6.1.1 avec codec VVC jusqu'à 25% plus rapide
- optimisation envoi commandes mqtt (start plus rapide)
- ajout offset fréquence emission

version 3.04
- correction bug sur calcul Fréquence hors PlutoDVB2
- modification et reboot suite changement indicatif sur PlutoDVB2
- Ajout différents SR SR1700 SR3000 SR5000
- Modification stop sur débit trop bas
- réglage seuils automatiques
- Modification métadonnées par défaut

version 3.05
- Ajout DVBS sur dernier firmware PlutoDVB2
- Lecture Temperature chip Analog Device sur firmware PlutoDVB2
- Ajout option Quick Tune avec lancement automatique
- choix fréquence et SR avec Quick Tune > créer line recepteur avec ip 127.0.0.1 port 9920
- correction bug sur mémorisation paramètres
- Réglage débit ffmpeg max en vbr
- ajout réglage Fec minimum en Fec Auto

version 3.06
- Correction bug sur codage AV1 soft qui plante..
- Installation silencieuse Eclipse Mosquitto
- vérification communication avec PlutoDVB2 pour éviter blocage Start avec message ou blocage sur Exit 
- ffmpeg Debug fermeture cmd sur STOP ou START+ pour visualiser si plantage
- affichage des valeurs monitoring plus stable
- b_ref_mode disabled pour certaines cartes NVIDIA

version 3.07
- Refonte graphique avec nouvel Onglet (separation Onglet PTT et Monitoring)
- déplacement certaines commandes
- Ajout lecture paramètres Device: version , Firmware , buffer
- Ajout démarrage auto OBS

Version 3.08
- Ajout paramètres preset ffmpeg
- Ajout réglage coordonnées x y d'ouverture dans fichier param.ini
- Ajout SDR HackRF (ajout dll modification Python GNU et progamme principal)
- Réactivation Offset dans param.ini pour version publié finale
