# Norl

Navigateur web pour Windows, inspiré d'Arc : onglets verticaux, espaces, dossiers, aperçu des liens, bloqueur de publicités et une page de réglages pour tout personnaliser. Construit sur Electron (moteur Chromium).

Ce dépôt ne contient que les installeurs de Norl et ce mode d'emploi.

## Installer

1. **[Télécharger la dernière version](https://github.com/EzvinSollier/Norl-versions/releases/latest)** : dans « Assets », le fichier `Norl-Setup-X.Y.Z.exe`.
2. Lancer l'installeur. Windows affiche « Windows a protégé votre ordinateur » (SmartScreen), parce que l'installeur n'est pas signé (la signature est payante) : cliquer sur **Informations complémentaires**, puis **Exécuter quand même**.
3. Choisir le dossier d'installation. Un raccourci Norl est créé sur le bureau et dans le menu Démarrer.

## Mises à jour

Norl vérifie au démarrage, puis toutes les heures, si une nouvelle version est publiée. Si oui, une petite icône apparaît à droite du bouclier, dans la barre d'adresse ; son infobulle liste les nouveautés.

- Un clic télécharge la mise à jour en arrière-plan (on continue de naviguer).
- Quand l'icône devient verte (« Redémarrer pour installer »), un clic ferme Norl, installe la nouvelle version et le rouvre avec les mêmes onglets.
- Rien ne s'installe sans ce clic. Les favoris, l'historique et les réglages sont gardés.
- Réglages → Mises à jour : la version installée et « Voir les nouveautés » (la liste de toutes les versions).

## Fonctionnalités

- **Espaces** : chaque espace a ses onglets, ses favoris épinglés, sa couleur et son propre profil (cookies, comptes, cache, historique séparés). Pastilles en bas de la barre latérale, clic droit pour renommer, changer la couleur ou supprimer (ses données sont effacées avec lui).
- **Dossiers d'onglets** : clic droit sur un onglet → « Créer un dossier » (il prend le nom de l'onglet). Clic droit sur le dossier pour le renommer, changer sa couleur ou le supprimer (fermer ses onglets ou les garder). On y range les onglets en les glissant ou par clic droit ; un lien ouvert depuis un onglet de dossier y reste. Les dossiers et leurs onglets reviennent au lancement, en veille (rien ne se charge avant un clic).
- **Aperçu (Peek)** : Maj+clic sur un lien l'ouvre dans une fenêtre flottante par-dessus la page, sans créer d'onglet. ✕, Échap ou un clic à côté la ferment ; ⤢ l'ouvre en onglet sans la recharger. Pendant l'aperçu, la barre d'adresse et le cadenas montrent sa page.
- **Espace privé** (bouton masque de la barre latérale) : ni historique ni cookies gardés ; tout est effacé quand il se ferme (clic droit, ou dernier onglet fermé).
- **Historique** dans `norl://history` (Ctrl+H) : l'historique de l'espace, avec recherche ; la palette ne propose que celui de l'espace affiché.
- **Vue scindée** : glisser un onglet sur la page l'ouvre à gauche ou à droite ; séparateur déplaçable (double-clic pour centrer).
- **Bloqueur de publicités et de traqueurs** (EasyList/EasyPrivacy) : bouclier dans la barre d'adresse avec le nombre d'éléments bloqués, désactivable par site.
- **Téléchargements** : enregistrés directement dans le dossier Téléchargements, progression dans la barre latérale, liste complète dans `norl://downloads`.
- **Confort** : recherche dans la page (Ctrl+F, Tab / Maj+Tab pour passer d'un résultat à l'autre), icône 🔊 / 🔇 sur les onglets qui jouent du son, mise en veille des onglets cachés depuis 5 minutes (réglable, jamais pour Discord ni pour un onglet qui joue du son ou où tu as commencé à taper).
- **Sécurité** : carte du site (clic sur le cadenas) avec permissions par site demandées à la volée, HTTPS uniquement, pages d'erreur de certificat, cookies tiers à la demande, liens nettoyés, DNS chiffré en option, confirmation avant d'ouvrir un fichier exécutable. L'installeur durcit Norl.exe (Electron Fuses).
- **Thèmes** : une bibliothèque de thèmes de couleurs (Catppuccin, Nord, Dracula, Gruvbox, Tokyo Night, Rosé Pine, Solarized, GitHub…) et de thèmes complets (couleurs, polices, arrondis, marges), un thème pour le jour et un pour la nuit, essai en direct au survol, thèmes perso à créer, importer et exporter (`.norl-theme.json`). Transparence Mica ou Acrylique de Windows 11, avec son niveau.
- **Densité** de l'interface : Compact, Normal ou Aéré.
- **Mots-clés de recherche** dans la palette et l'adresse : `!gh norl` cherche sur GitHub, `!claude`, `!gemini`, `!yt`, `!w` (Wikipédia), `!asura`, `!discord` ; liste modifiable dans les réglages.
- **Réglages** dans `norl://settings` (bouton ⚙) : moteur de recherche, thème, couleurs, disposition, espaces, bloqueur, téléchargements, démarrage, avec une recherche en haut de la page. Section « Données » : taille du cache de chaque espace, vider le cache, effacer l'historique ou les cookies et données des sites (déconnecte les comptes de l'espace), taille maximale du cache.

## Raccourcis

Raccourcis par défaut, modifiables dans `norl://settings` → Raccourcis (sauf Ctrl+chiffre, Ctrl+Maj+chiffre et le zoom, liés à la touche physique).

| Raccourci | Action |
| --- | --- |
| Ctrl+T | Palette : nouvel onglet, historique, commandes du navigateur |
| Ctrl+L | Modifier l'adresse |
| Ctrl+W | Fermer l'onglet (sans onglet ouvert : fermer le navigateur) |
| Ctrl+Maj+T | Rouvrir le dernier onglet fermé (même après redémarrage) |
| Ctrl+D | Épingler / retirer la page des favoris de l'espace |
| Ctrl+Maj+1…9 | Aller à l'espace n |
| Ctrl+Maj+S | Vue scindée : onglet actif et précédent côte à côte / fermer |
| Ctrl+, | Réglages |
| Ctrl+J | Téléchargements |
| Ctrl+H | Historique de l'espace |
| Ctrl+F | Rechercher dans la page (Tab : suivant, Maj+Tab : précédent) |
| Ctrl+M | Couper / remettre le son de l'onglet |
| Ctrl+S | Afficher/masquer la barre latérale (masquée, elle réapparaît au survol du bord) |
| Ctrl+Tab / Ctrl+Maj+Tab | Onglet suivant / précédent |
| Ctrl+1…8, Ctrl+9 | Aller à l'onglet n / au dernier (touches physiques : fonctionne aussi en AZERTY) |
| Alt+← / Alt+→ | Précédent / suivant |
| Ctrl+R, F5 / Ctrl+Maj+R | Actualiser / sans cache |
| Ctrl+= / Ctrl+- / Ctrl+0 | Zoom |
| F12 | Outils de développement de la page |
| Ctrl+Maj+I (depuis l'interface) | Outils de développement de l'interface |

## Personnalisation et données

La page `norl://settings` (bouton ⚙, Ctrl+,) couvre les réglages courants. Tout est enregistré dans `%APPDATA%\Norl\` (bouton « Ouvrir le dossier » dans les réglages) :

- `settings.json` : tous les réglages, modifiables à la main (rechargés à chaud).
- `userChrome.css` : CSS libre appliqué à l'interface.
- `sites/<domaine>.css` et `sites/<domaine>.js` : CSS et JavaScript personnels par site (`youtube.com.css` s'applique à YouTube et à ses sous-domaines). Depuis une page : Ctrl+T puis « Modifier le CSS de ce site ».

## Désinstaller

Paramètres Windows → Applications → Applications installées → Norl → Désinstaller. Les données de `%APPDATA%\Norl` restent : les supprimer à la main pour tout effacer.

## Limites connues

- Pas de Netflix, Disney+ ni autre vidéo protégée (Widevine absent).
- Pas d'extensions Chrome.
- Installeur non signé : avertissement SmartScreen à la première installation.
