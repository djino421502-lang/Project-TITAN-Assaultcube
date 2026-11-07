# TITAN pour AssaultCube — mode local hors ligne

Ce dépôt contient le patch source de TITAN pour AssaultCube et les instructions pour l'essayer. Il ajoute un adversaire TITAN au mode Deathmatch solo, des tactiques de combat locales et un repère visuel sur la carte.

TITAN réutilise la navigation, la perception et la visée natives d'AssaultCube. Ce patch n'utilise pas le checkpoint Q du simulateur éducatif TITAN. Il est destiné aux parties locales hors ligne. Il n'ajoute pas de bot réseau et ne doit pas servir à obtenir un avantage sur des serveurs publics.

## Fichiers inclus

- `titan_bot.patch` — changements TITAN seulement, sous forme de patch à appliquer au code source officiel.
- `README.md` — ces instructions.

Le dépôt ne contient ni le jeu, ni ses cartes, sons, textures, modèles, exécutables, ni les données d'apprentissage TITAN.

## Préparer le code source

1. Installe Git et les outils Visual Studio C++ nécessaires pour compiler AssaultCube sous Windows.
2. Clone le dépôt officiel d'AssaultCube dans un dossier séparé :

   ```powershell
   git clone https://github.com/assaultcube/AC.git assaultcube
   ```

3. Ouvre PowerShell dans le dossier `assaultcube` et applique le patch téléchargé depuis ce dépôt TITAN :

   ```powershell
   git apply --check C:\chemin\vers\TITAN-AssaultCube\titan_bot.patch
   git apply C:\chemin\vers\TITAN-AssaultCube\titan_bot.patch
   ```

   Remplace `C:\chemin\vers\TITAN-AssaultCube` par l'emplacement où tu as téléchargé ce dépôt.

4. Compile le client avec le projet Visual Studio fourni par AssaultCube, puis lance le jeu localement.

5. Dans le menu **Singleplayer**, choisis **TITAN Deathmatch (local)**, puis une carte.

La commande `addtitanbot` ajoute également TITAN à un match solo compatible. Dans le jeu, `F11` ouvre la console. `Alt gauche` affiche la carte complète et le repère TITAN.

## Origine et licences

AssaultCube est un projet indépendant. Ce dépôt n'est ni officiel ni approuvé par ses développeurs. Le code original reste soumis à ses propres avis de licence ; consulte les fichiers de licence du dépôt officiel et la [page de licence d'AssaultCube](https://assault.cubers.net/docs/license.html) avant de redistribuer une version modifiée ou compilée. Les ressources du jeu ont des licences distinctes et ne sont pas incluses ici.

Le projet TITAN est fourni sans garantie. Le patch est prévu pour un usage local hors ligne ; ne connecte pas un client modifié à des serveurs publics.
