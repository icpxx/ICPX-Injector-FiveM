 ICPX Lua Panel — archive x64 / x64 archive

**Français ci-dessous · English below the French section**

## Français

Cette archive contient le **panneau ICPX déjà compilé** avec son éditeur Lua,
ses pages d'options et les DLL dont elles dépendent. Il s'agit du binaire
Release x64 construit le **25 septembre 2026 à 19:17**. Aucun nouveau build
n'a été effectué pour créer cette archive.

## Installation

1. Extraire **tous** les fichiers du `.rar` dans un même dossier. Ne pas
   démarrer `ICPX_panel.exe` directement depuis WinRAR.
2. Lancer FiveM, puis `ICPX_panel.exe` depuis ce dossier. Accepter l'invite
   Windows d'administration si elle apparaît.
3. Dans FiveM, appuyer sur **INSERT** pour afficher ou masquer le panneau.

Le panneau et ses ponts natifs sont conçus pour le build FiveM **b3751** ;
leur fonctionnement n'est pas garanti après une mise à jour du jeu.

## Scripts et Lua

- **Scripts > Load** ouvre `icpx_menu.lua`, inclus dans l'archive, dans
  l'éditeur du panneau.
- **Éditeur / Run** exécute le code dans le Lua **intégré au panneau**. Le
  résultat de `print(...)` apparaît localement et peut être transmis à F8.
- **Save file** enregistre ton texte dans un fichier `.lua` de ton choix.
- **Test F8** écrit `icpx : hello word` dans la console F8 via
  `ICPX_input_hook.dll`. Cette opération affiche une ligne, elle n'exécute
  pas une commande FiveM.
- **Sonde Lua passive** observe des chargements de scripts ; elle ne lance
  pas ton code dans une ressource.

**Run n'exécute pas Lua dans le runtime des ressources FiveM.** Les natives
du jeu et les fonctions des ressources ne sont pas disponibles dans ce Lua
isolé. Charger `icpx_menu.lua` ne modifie aucune ressource du serveur.

## Autres pages

- **Visual / options du panneau** : interface et réglages disponibles dans
  l'exécutable fourni. Les fonctions natives demandent
  `ICPX_native_noclip_v26.dll`, inclus dans l'archive.
- **Resources** : affiche des ressources visibles côté client et lit des
  informations du cache local ; cela ne donne pas accès aux scripts qui
  restent uniquement sur le serveur.
- **Settings** : contient notamment Block Input, les réglages du panneau,
  Streamproof et les raccourcis.
- **Chat All** : nécessite un relais distinct. Pour le configurer, placer
  `chat_relay_url.txt` à côté de l'exécutable avec l'URL HTTPS de ce relais
  sur une seule ligne. Ce fichier n'est pas fourni dans l'archive.

## Fonctions indisponibles dans cette archive

`ICPX_event_hook.dll` est volontairement absent : son activation a été
suivie d'un crash de FiveM lors des essais. **Start / Stop des ressources,
blocage de leur démarrage, Event Bypass et Block ScreenShot ne fonctionnent
pas ici.** Ce binaire a été compilé avant la dernière correction de
l'interface : le bouton Block ScreenShot peut encore être visible, mais
son module n'est pas fourni. Les sources plus récentes le grisent ; il faut
que le propriétaire reconstruise le panneau pour voir cette correction.

## Fichiers fournis

| Fichier | Rôle |
| --- | --- |
| `ICPX_panel.exe` | Panneau et éditeur Lua |
| `icpx_menu.lua` | Exemple de configuration du menu |
| `ICPX_input_hook.dll` | Relais F8 et Block Input |
| `ICPX_native_noclip_v26.dll` | Fonctions natives des pages concernées |
| `ICPX_runtime_probe_passive_v11.dll` | Sonde Lua passive |

Aucune configuration personnelle, sauvegarde locale ni fichier du serveur
n'est inclus.

---

## English

This archive contains the **already-built ICPX panel**, its Lua editor,
options pages, and supporting DLLs. The Release x64 executable was built on
**September 25, 2026 at 19:17**. No new build was run to create this archive.

### Installation

1. Extract **all** files from the `.rar` into the same folder. Do not run
   `ICPX_panel.exe` directly from WinRAR.
2. Start FiveM, then run `ICPX_panel.exe` from that folder. Accept the Windows
   administrator prompt if it appears.
3. In FiveM, press **INSERT** to show or hide the panel.

The panel and native bridges target FiveM build **b3751**. They are not
guaranteed to work after a game update.

### Scripts and Lua

- **Scripts > Load** opens the included `icpx_menu.lua` in the panel editor.
- **Editor / Run** executes code in the Lua interpreter **inside the panel**.
  Output from `print(...)` appears locally and can be forwarded to F8.
- **Save file** saves your text to a `.lua` file you choose.
- **Test F8** writes `icpx : hello word` to the F8 console through
  `ICPX_input_hook.dll`. Printing this line does not execute a FiveM command.
- **Passive Lua probe** observes script loading; it does not run your code
  inside a resource.

**Run does not execute Lua in FiveM's resource runtime.** Game natives and
resource functions are unavailable to this isolated Lua interpreter. Loading
`icpx_menu.lua` does not modify any server resource.

### Other pages

- **Visual / panel options:** the settings available in the included
  executable. Features that need the native bridge use the included
  `ICPX_native_noclip_v26.dll`.
- **Resources:** shows resources visible on the client and reads local cache
  information. It cannot access scripts kept only on the server.
- **Settings:** includes Block Input, panel settings, Streamproof, and hotkeys.
- **Chat All:** requires a separate relay. To configure one, place a
  `chat_relay_url.txt` file beside the executable containing the relay's
  HTTPS URL on a single line. This file is not included.

### Unavailable features in this archive

`ICPX_event_hook.dll` is intentionally excluded: enabling its detour was
followed by a FiveM crash during testing. **Resource Start / Stop, blocking
resource starts, Event Bypass, and Block ScreenShot do not work in this
archive.** This executable predates the latest UI change: the Block
ScreenShot control may still be visible, but its required module is absent.
The newer source code disables that control; the owner must rebuild the panel
to see the UI change.

### Included files

| File | Purpose |
| --- | --- |
| `ICPX_panel.exe` | Panel and Lua editor |
| `icpx_menu.lua` | Sample menu configuration |
| `ICPX_input_hook.dll` | F8 relay and Block Input |
| `ICPX_native_noclip_v26.dll` | Native features used by the relevant pages |
| `ICPX_runtime_probe_passive_v11.dll` | Passive Lua probe |

No personal configuration, local saves, or server files are included.
