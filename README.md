# CRYPTOHACK


# Description du projet

Ce script Python permet de vérifier la version de Python en cours d'exécution et de générer un texte "flag" à partir d'une série de valeurs chiffrées. Il est conçu pour sensibiliser les utilisateurs à l'utilisation de Python 3 et à la manipulation de bases numériques dans les calculs. 

## Fonctionnalités
- Avertit l'utilisateur si le script est exécuté sous Python 2, qui n'est plus supporté.
- Génère un texte à partir d'une série de valeurs chiffrées en appliquant une opération de déchiffrement simple utilisant le XOR (^) en base 16.

## Prérequis

- Python 3.x doit être installé sur votre machine.

## Utilisation

Pour exécuter ce script, utilisez la commande suivante dans un terminal :

```bash
python3 script.py
```

Si vous exécutez le script sous Python 2, il vous demandera de mettre à jour vers Python 3.

## Explication du code

1. **Vérification de la version de Python**  
   Le script commence par vérifier si vous exécutez une version obsolète de Python (Python 2). Cette vérification est faite grâce à la bibliothèque `sys` :

   ```python
   if sys.version_info.major == 2:
       print("You are running Python 2, which is no longer supported. Please update to Python 3.")
   ```

2. **Tableau de nombres (ordonnées)**  
   Un tableau `ords` contient une série de valeurs entières qui représentent des caractères chiffrés :

   ```python
   ords = [81, 64, 75, 66, 70, 93, 73, 72, 1, 92, 109, 2, 84, 109, 66, 75, 70, 90, 2, 92, 79]
   ```

3. **Opération XOR pour déchiffrer le flag**  
   Le code utilise une opération **XOR** (^) entre chaque entier de la liste `ords` et la valeur hexadécimale `0x32` (50 en décimal).  
   
   L'opérateur XOR est souvent utilisé en cryptographie pour chiffrer ou déchiffrer des données. L'idée est que lorsque vous appliquez XOR avec la même clé sur un texte chiffré, vous récupérez le texte original.

   - **XOR entre deux nombres :**  
     L'opération XOR effectue une comparaison bit à bit entre deux nombres. Si les bits sont identiques, le résultat est 0, sinon 1.

   Exemple :
   ```python
   print(chr(o ^ 0x32) for o in ords)
   ```

   Chaque élément du tableau `ords` est XOR avec `0x32`, ce qui transforme le résultat en un caractère lisible grâce à la fonction `chr()`.

4. **Affichage du résultat**  
   Enfin, le script concatène tous les caractères déchiffrés pour afficher le "flag" final :

   ```python
   print("Here is your flag:")
   print("".join(chr(o ^ 0x32) for o in ords))
   ```

   Le flag obtenu est le résultat de cette opération XOR.

## Bases numériques et calculs

- **Décimal** : Le système de numérotation que nous utilisons tous les jours, basé sur 10 chiffres (0-9).
- **Hexadécimal (base 16)** : Utilisé principalement en informatique, il représente les nombres en utilisant 16 symboles (0-9 et A-F). Par exemple, `0x32` en hexadécimal vaut `50` en décimal.
- **XOR (^)** : L'opérateur XOR effectue une comparaison bit à bit entre deux nombres. Dans ce cas, on effectue un XOR entre chaque élément de `ords` et `0x32` pour déchiffrer les caractères chiffrés.

## Exécution

Le script affichera un "flag" comme résultat à partir de la liste donnée de nombres chiffrés.

## Contribution

Les contributions sont les bienvenues ! Si vous avez des idées pour améliorer ce script, n'hésitez pas à soumettre une demande de modification (pull request).
