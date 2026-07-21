# Murmur — installation

Dictée vocale locale pour macOS : tu maintiens une touche, tu parles, le texte s'écrit
dans l'app active. Tout se passe sur ta machine — aucun serveur, aucun compte, rien
qui sorte du Mac.

## Prérequis (à vérifier avant tout)

- **macOS 26 (Tahoe) ou plus récent** — obligatoire, l'app utilise le moteur de
  transcription intégré à cette version. Sur macOS 15 ou antérieur, elle ne démarrera pas.
- **Mac Apple Silicon** (M1 ou plus récent).
- **Apple Intelligence activé** — optionnel : sans lui, la dictée fonctionne mais le
  texte est collé brut, sans reformatage.

## Installation

1. Décompresse l'archive et **glisse `Murmur.app` dans ton dossier Applications**.

2. **Lance l'app** (double-clic). Elle est signée et notarisée par Apple, donc elle
   s'ouvre normalement, sans avertissement de sécurité.

   Rien ne s'affiche à l'écran : c'est normal, Murmur vit uniquement dans la barre de
   menus. Cherche l'icône **🎙 micro** en haut à droite, près de l'horloge. Si tu ne la
   vois pas, elle est peut-être masquée près de l'encoche : ferme une autre app à icône,
   ou fais ⌘ + glisser pour réorganiser la barre.

3. **Accorde les trois permissions.** macOS va les demander ; il faut les trois :

   | Permission | À quoi ça sert | Où l'activer |
   |---|---|---|
   | **Microphone** | Entendre ta voix | Popup au 1er lancement |
   | **Surveillance de la saisie** | Détecter le raccourci | Réglages Système → Confidentialité et sécurité → Surveillance de la saisie |
   | **Accessibilité** | Coller le texte | Réglages Système → Confidentialité et sécurité → Accessibilité |

   Le menu de Murmur affiche un bandeau ⚠️ cliquable tant qu'une permission manque —
   il t'emmène directement au bon réglage.

4. Au premier lancement, le **modèle de reconnaissance français se télécharge** tout
   seul (une fois, quelques dizaines de Mo).

## Utilisation

**Maintiens la touche ⌥ Option droite**, parle, **relâche** → le texte est transcrit,
corrigé selon le mode actif, et collé là où est ton curseur.

Un son « Tink » signale le début, un « Pop » le collage. Les appuis de moins de 0,4 s
sont ignorés (anti-fausse-manip), et ton presse-papiers est restauré après le collage.

### Le menu 🎙

- **Modes** : choisis comment ton texte est retouché — *Brut* (aucune retouche),
  *Brut corrigé*, *Email*, *Notes*, *Prompt IA*.
- **Éditer les modes…** (⌘,) : crée tes propres modes. Un mode = un nom + une consigne
  en français décrivant la retouche voulue. Consigne vide = collage direct.
- **Historique** : tes dernières dictées ; un clic recopie le texte.
- **Langue** : français / anglais.
- **Déclencheur souris** : active le clic molette en plus du clavier
  (tap = démarre/arrête en mains libres, maintien = dicte le temps du clic).

## Conseils

- **Évite les AirPods comme micro.** En Bluetooth, leur micro bascule en mode « mains
  libres » très dégradé et la transcription devient vide ou fausse. Va dans
  Réglages Système → Son → **Entrée** et choisis le micro intégré du Mac.
- **Lancement au démarrage** : Réglages Système → Général → Ouverture et extensions →
  ajoute Murmur.

## En cas de souci

Un journal détaillé est écrit ici :

```
~/Library/Application Support/Murmur/murmur.log
```

Il note chaque appui, chaque transcription, le niveau sonore capté et l'état des
permissions — de quoi diagnostiquer à peu près n'importe quoi.
