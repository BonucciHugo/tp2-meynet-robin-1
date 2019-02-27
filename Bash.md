# Script Bash - Meynet/Devillebichot

  ## Exercice 1: Variables d'environnement
  
  1. Les commandes tapées par l'utilisateur sont contenues dans le dossier _/bin_.
  
  2. La commande ```cd``` tapée sans arguments utilise la variable d'environnement _$HOME_ pour revenir à notre répertoire personnel.
  
  3. Voyons à quoi servent ces variables d'environnement:
      * LANG : contient la langue d'installation du système et l'encodage, en l'occurrance _fr'_FR.UTF-8_.
      * PWD : contient le chemin courant dans lequel on se trouve.
      * OLDPWD : contient le chemin courant précédant.
      * SHELL : contient le type de shell utilisé par le système (ex: bash, sh etc.).
      * _ : contient le dernier argument de la dernière commande exécutée.
      
  4. On peut créer une variable **locale** en utilisant la commande ```MY_VAR="abcdef1234"```.
  
  5. La commande ```bash``` permet d'ouvrir un terminal utilisant le bash. La variable créée précédement n'est plus présente car c'est une variable **locale** et non **d'environnement**.
  
  6. On transforme notre variable précédente en variable **d'environnement** en utilisant la commande ```export MY_VAR="$MY_VAR"```. Lorsque que l'on effectue les tests de la question 5 on voit que la variable reste même si l'on ouvre une nouvelle session de bash. C'est l'utilité de la variable d'environnement.
  
  7. On crée la variable _NOMS_ avec la commande ```export NOMS="Meynet Devillebichot"```.
  
  8. En utilisant la commande ```echo "Bonjour à vous deux, $NOMS !"``` on interprète la variable _$NOMS_ car on utilise les double quote **"**.
  
  9. La différence entre un ```unset``` et l'affection d'une valeur vide est simple: unset supprime la variable d'environnement alors que dans le second cas, on affecte simplement une valeur (certe vide) à la variable **mais elle existe toujours**.
  
  10. Pour afficher _$HOME = chemin_ il faut utiliser un caratère d'échappement: ```echo "\$HOME = $HOME"```. Ainsi _\$HOME_ ne sera pas interprétée.
  
  ## Programmation bash
  ## Exercice 2: Contrôle de mot de passe.
  
  ```
     #! /bin/bash
     PASSWORD = 'toto'
     read -p 'Entrez votre mot de passe: " -s a
     if [ $PASSWORD = $a ]; then
          echo "Bienvenue $USER"
     else
          echo 'mauvais mdp'
     fi
  ```
  
  
  
