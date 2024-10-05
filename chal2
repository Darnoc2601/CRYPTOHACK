# Conversion de nombres ASCII en texte

Ce script Python convertit une liste de nombres ASCII en une chaîne de caractères lisible.

## Description

Le code source prend une liste de nombres entiers représentant des caractères ASCII, les convertit en leurs caractères correspondants, puis concatène ces caractères pour former une chaîne de texte finale.

## Code source

```python
# Tableau d'entiers ASCII
ascii_numbers = [99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]

# Conversion des entiers en caractères ASCII
flag = "".join(chr(num) for num in ascii_numbers)

# Affichage du flag
print(flag)
```

## Fonctionnement

1. **Définition des données d'entrée** :
   - `ascii_numbers` est une liste de nombres entiers représentant des caractères ASCII.

2. **Conversion en caractères** :
   - La ligne `flag = "".join(chr(num) for num in ascii_numbers)` effectue la conversion :
     - `chr(num)` convertit chaque nombre en son caractère ASCII correspondant.
     - Une compréhension de liste `(chr(num) for num in ascii_numbers)` applique cette conversion à tous les nombres.
     - `"".join(...)` concatène tous les caractères en une seule chaîne.

3. **Affichage du résultat** :
   - `print(flag)` affiche la chaîne de caractères obtenue.

## Utilisation

Pour utiliser ce script :

1. Assurez-vous d'avoir Python installé sur votre système.
2. Copiez le code dans un fichier `.py` (par exemple, `ascii_converter.py`).
3. Exécutez le script en utilisant la commande : `python ascii_converter.py`
4. Le résultat sera affiché dans la console.

## Note

Ce code semble être utilisé pour décoder un "flag", probablement dans le contexte d'un défi de cryptographie ou de sécurité informatique.
