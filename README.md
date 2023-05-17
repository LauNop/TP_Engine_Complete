# TP Engine

## Vis
*Dans un script __ScrewManager__*
1. Faire en sorte, à l'aide d'un raycast, qu'un clique gauche sur une vis la désactive (gameObject.SetActive(false)).
2. Lorsque toutes les vis sont désactivées, invoquer un événement publique dont pourront se servir d'autres scripts. Attention à n'appeler l'événement qu'une fois quand l'état change.

## Séparation du moteur

*Dans un script __EngineSplitting__*
1. Ajouter une fonction qui écoute l'événement de la partie **Vis**, appelé lorsque toutes les vis sont désactivées.
2. Cette fonction doit séparer le moteur en plusieurs parties progressivement à l'aide d'un lerp.
3. *Bonus : Chercher un moyen de transformer le lerp (linéaire) en un courbe smoothée. Le nom technique est ease-in/out.*

## Camera

*Dans un script __CameraControls__*

1. Faire en sorte que l'on puisse faire tourner la camera horizontalement autour du moteur avec les fléches horizontales.
2. Faire en sorte que les fléches verticales permettent de monter ou descendre la camera (dans l'espace du monde).
3. Limiter la translation à maximum 2 mètres vers le haut et vers le bas (de -2 à +2).
4. Faire en sorte que la camera regarde en permanance l'origine du monde grace à la fonction *LookAt()*.

## Allumage

1. Créer un bouton qui doit activer ou désactiver le highlight des vis. Pour ce faire, le bouton doit appeler la fonction *SetHighlight()* du composant *ScrewHighlight*. Le text du bouton doit changer en fonction.
2. Créer un slider qui permette de controller la vitesse du moteur.

