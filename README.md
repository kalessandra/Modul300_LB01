# Dokumentation LB01 Modul 300 Kalasch

# Table of contents
1. [Installierte Applikationen](#applikationen)
   1. [GitHub Account](#subparagraph1)
2. [Linux](#paragraph1)
3. [Virtualisierung](#paragraph2)
4. [Vagrant](#paragraph3)
   1. [Installationsanleitung](#subparagraph2)
   2. [Vagrantbefehle](#subparagraph3)
5. [Testing](#paragraph4)
6. [Umgebung](#paragraph5)
7. [Versionsverwaltung / Git](#paragraph6)
8. [Mark Down](#paragraph7)
9. [Systemsicherheit](#paragraph8)
10. [Vergleich Vorwissen](#paragraph9)  
11. [Refelxion](#paragraph10)   

## Installierte Applikationen <a name="applikationen"></a>
VirtualBox  <br>
Vagrant  <br>
Visualstudio-Code  <br>
Git-Client  <br>
SSH-Key für Client erstellt  <br>

### GitHub Account <a name="subparagraph1"></a>
Ein GitHub Account wurde erstellt.

## Linux <a name="paragraph1"></a>
Ich habe jetzt schon häufiger mit Linux gearbeitet, desshalb ist es nicht so schwer, die Befehle für diverse Installationen usw. zu wissen. 


## Virtualisierung <a name="paragraph2"></a>
Ich habe schon in diversen Modulen das Thema Virtualisierung gehabt. Wir haben Server, Worksations, etc. virtualiesiert.  <br>
Unter Virtualisierung versteht man die Bereitstellung von physikalischen Hardwareressourcen für virtuelle Maschinen. Dabeikann es sich um ein oder mehrere eigenständige Gastsysteme handeln. Die Gastsysteme („VMs“= Virtual Machines) wissen nichts von ihrer virtuellen Existenz und verhalten sich wie „echte“ Server.

## Vagrant <a name="paragraph3"></a>
Vagrant wird zum Erstellen und Verwalten von virtuellen Maschienen verwendet. Vagrant wird über eine Shell gesteuert. 

### Installationsanleitung <a name="subparagraph2"></a>
vagrant box add ubuntu/trusty64 --name ubuntu/trusty64  <br>
vagrant init ubuntu/trust64  <br>
vagrant up  <br>
vagrant ssh  <br>
apt-get update  <br>
sudo debconf-set-selections <<< 'mysql-server mysql-server/root_password password root'  <br>
sudo debconf-set-selections <<< 'mysql-server mysql-server/root_password_again password root'  <br>
apt-get install -y mysql-client mysql-server  <br>
mysqladmin create modul300lb01 --user=root --password=root --host=127.0.0.1 --protocol=tcp  <br>
mysql -h localhost -u root -proot modul300lb01test  <br>
apt-get install ufw  <br>
sudo ufw --force enable  <br>
sudo ufw allow 80/tcp <br>


### Vagrant Befehle <a name="subparagraph3"></a>

| Befehle | Beschreibung
| ------- | -----------
| vagrant init | Initialisiert im aktuellen Verzeichnis eine Vagrant-Umgebung und erstellt, falls nicht vorhanden, ein Vagrantfile
| vagrant up | Erzeugt und Konfiguriert eine neue Virtuelle Maschine, basierend auf dem Vagrantfile
| vagrant ssh | Baut eine SSH-Verbindung zur gewünschten VM auf
| vagrant status | Zeigt den aktuellen Status der VM an
| vagrant port | Zeigt die Weitergeleiteten Ports der VM an
| vagrant halt| Stoppt die laufende Virtuelle Maschine
| vagrant destroy | Stoppt die Virtuelle Maschine und zerstört sie.


## Testing <a name="paragraph4"></a>
| Testfall | Funktioniert / Nicht Funktioniert
| ------- | -----------
| Datenbank erstellen | Eine Datenbank konnte erfolgreich erstellt werden
| Installation läuft ohne Fehler | Die Installation der Datenbank läuft ohne Fehler
| Firewall Installation erfolgreich | Die Firewall wurde erfolgreich installiert

## Umgebung <a name="paragraph5"></a>
Meine VM ist eine einfache Datenbank. Auf meiner VM läuft MySQL. Im Vagrantfile steht, was alles gemacht wurde. Auf diese Datenbank kann man via SSH zugreifen.



## Versionsverwaltung / Git <a name="paragraph6"></a>
Auf Github sieht man wenn ich etwas hochgeladen oder verändert habe. 

## Mark Down <a name="paragraph7"></a>
Markdown ist eine vereinfachte Auszeichnungssprache, die von John Gruber und Aaron Swartz entworfen und im Dezember 2004 mit Version 1.0.1 spezifiziert wurde. Ein Ziel von Markdown ist, dass schon die Ausgangsform ohne weitere Konvertierung leicht lesbar ist.

## Systemsicherheit <a name="paragraph8"></a>
The second paragraph text

## Vergleich Vorwissen <a name="paragraph9"></a>
Vor diesem Modul hatte ich mich nicht gross mit Vagrant auseinandergesetzt, weil ich es noch nicht kannte. Dadurch ist es eher schwer für mich, mich damit ausaneinander zu setzten. In diesem Modul habe ich es aber kennengelert und weiss jetzt auch wie ich es verwenden kann. Ich habe viel neues dazu gelerent.


## Reflexion <a name="paragraph10"></a>
Es war schwer, sich mit Vagrant auseinanderzusetzten, weil ich das noch nie verwendet habe. Ich hatte am Anfag Schwierigkeiten, eine VM aufzusetzten, weil es nie so funktioniert hat, wie es sollte. Später mit Hilfe von Recherchen und auch dem Lehrer, habe ich es geschafft, eine VM aufzusetzten und sie machte auch das was sie sollte. Mit Markdown hatte ich keine Probleme, weil es nicht sehr schwierig ist damit zu arbeiten. Diese LB hat mir gezeigt, was man mit Vagrant und Markdown alles machen kann.
