## vps-hardening
### Härten eines V Servers im Internet

als Erstes wie immer das System updaten

sudo apt update && dist-upgrade
Anlegen eines neuen Benutzers

adduser username

sicheres Passwort setzen

die folgenden Abfragen kann man einfach weiterklicken
Benutzer der Gruppe sudo zuweisen

usermod -aG sudo
zum angelegten Account wechseln

su - username
zum Test lasse ich mir den Inhalt von /root anzeigen

sudo ls -la /root
SSH absichern

auf einem Linuxsystem folgendes ausführen:

ssh-keygen -t ed25519

sprechenden Namen des Key Paares festlegen

eine Passphrase (Passwort) setzen
Fortsetzung folgt
