# Script de connexion Virtualia

[Logo Virtualia](virtualia.gif)

Le script ne fait pas grand chose, mais permet de gagner quelques secondes 4 fois par jour.

Mon navigateur par défaut est Firefox, mais pour le script Virtualia, je préfère Chromium.
Cependant, le script doit aussi fonctionner avec Firefox (prendre le driver selenium pour firefox).

Depuis le site `https://sites.google.com/a/chromium.org/chromedriver/downloads`:

Télécharger `wget https://chromedriver.storage.googleapis.com/2.40/chromedriver_linux64.zip`

Dézipper le paquet dans le répertoire `lib`.

Installer `selenium` qui permet de contrôler le navigateur.
```bash
pip3 install selenium
```

Copier/coller `virtualia_menu_gnome.desktop` vers le menu de gnome. Éditer le fichier:
```bash
cp virtualia_menu_gnome.desktop.template ~/.local/share/applications/virtualia_menu_gnome.desktop
vim ~/.local/share/applications/virtualia_menu_gnome.desktop
```

* VIRTUALIA_NOM
* VIRTUALIA_PRENOM
* VIRTUALIA_PASSWORD
* et le chemin vers le script python et l'image Virtualia

 ```bash
VIRTUALIA_NOM=TON_NOM VIRTUALIA_PRENOM=ton_prenom VIRTUALIA_PASSWORD=mot_de_passe /home/trimaille/dev/toolbox/venv/bin/python3.6 /home/trimaille/dev/toolbox/virtualia/badge.py
```
