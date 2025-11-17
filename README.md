# Font Installer

Script for quickly installing multiple fonts (compatible with Thunar and Nautilus).

<br><br>


## Installation:

               sudo mv usr /   or  sudo mv -i acao_font-installer.sh /usr/local/bin/

               sudo chmod +x /usr/local/bin/acao_font-installer.sh


------------------------------------------------------------------------------------------

## Xfce (configure)

mkdir -p ~/.config/Thunar/

nano ~/.config/Thunar/uca.xml
```
<action>
	<icon>/usr/share/icons/extras/fonts.jpg</icon>
	<name>Instalar Fonte</name>
	<submenu></submenu>
	<unique-id>1763354524864721-1</unique-id>
	<command>/usr/local/bin/acao_font-installer.sh %F</command>
	<description>Instalar fonte em ~/.fonts</description>
	<range>*</range>
	<patterns>*.ttf;*.otf;*.ttc;*.woff;*.woff2;*.pfb;*.pfa;*.pfm;*.afm;*.otc;*.bdf;*.pcf;*.snf</patterns>
	<other-files/>
</action>
```

Terminates any running instance of Thunar.

thunar -q

------------------------------------------------------------------------------------------

## Gnome (configure)

mkdir -p ~/.local/share/nautilus/scripts

ln -sf /usr/local/bin/acao_font-installer.sh ~/.local/share/nautilus/scripts/

Terminates all running instances of Nautilus.

nautilus -q

------------------------------------------------------------------------------------------

## How to use:           
               $ acao_font-installer.sh file.ttf file1.ttf file2.ttf 
               
## Requirements: 

               bash, yad, fc-list, fc-cache, zip, mv
