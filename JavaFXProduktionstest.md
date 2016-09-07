# **JavaFX Produktionstest in JabRef 3.6**
**WARNUNG - Die Fehlerquellen stammen von einer alten Version des JavaFX Branches und sind inzwischen größtenteils behoben!** 

Issue: [https://github.com/koppor/stupro-jabref/issues/2](https://github.com/koppor/stupro-jabref/issues/2)

Die folgenden Tests sollen bei der Entscheidung, die Portierung von JavaFX vorzuführen. Getestet wurden die Betriebssysteme mit VirtualBox (VirtualBox 5.1.2 for Windows hosts - https://www.virtualbox.org/).

## Getestete Elemente:

- Error Console                 ( [https://github.com/motokito/jabref/tree/ErrorConsoleDialogFX](https://github.com/motokito/jabref/tree/ErrorConsoleDialogFX))
  - Klick auf: Help-&gt; Show developer Information
  - Im Dialog: Copy Log testen &amp; Developer information ein-/ausblenden
- Aboutdialog                 ( [https://github.com/JabRef/jabref/tree/javafx](https://github.com/JabRef/jabref/tree/javafx))
  - Klick auf: Help-&gt; About JabRef
  - Im Dialog: Copy testen / Alle Reiter mit Variablen kontrolliern
- Customize Key Bindings Dialog ( [https://github.com/JabRef/jabref/tree/javafx](https://github.com/JabRef/jabref/tree/javafx))
  - Klick auf: Options-&gt; Customize key bindigs
- Mathscinet                 ( [https://github.com/JabRef/jabref/tree/javafx](https://github.com/JabRef/jabref/tree/javafx))
  - Klick auf: BibTeX-&gt; Customize entry types
  - Zufälligen hinzufügen und mit Beipiel Eintrag testen
- Groups rework javafx         ( [https://github.com/tobiasdiez/jabref/tree/groupsRework](https://github.com/tobiasdiez/jabref/tree/groupsRework))
  - Klick auf: Groups-&gt; Toggle groups interface
  - Schließen &amp; Untoggle testen
- Journal abbreviationsFX ( [https://github.com/boceckts/jabref/tree/JournalAbbreviationsFX](https://github.com/boceckts/jabref/tree/JournalAbbreviationsFX))
  - Klick auf: Options-&gt; Manage journal abbreviations-&gt; Remove list
  - IEEE built anzeigen &amp; Schließen

Diese Elemente sind auf dem Branch (https://github.com/bruehldev/jabref/tree/javafxTest) zu einer Version gemerged (http://bit.ly/2aYFVrC). Der Branch wurde am 26.07.2016 mit auf den master Branch von JabRef aktualisiert.

## Notwendige Pakete:

JavaFX ist nicht Teil anderer Versionen von Java(GNU, Sun, IceTea und wird nur mit dem JDK und JRE von Oracle unterstützt ( [http://www.oracle.com/technetwork/java/javafx/downloads/index.html](http://www.oracle.com/technetwork/java/javafx/downloads/index.html)). Auf folgender Seite ( [http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)) sind alle Versionen für die getesteten Betriebssysteme aufgelistet.

Eine andere Alternative wäre eine Ausführung mit openjdk und dem Zusatzpaket openjfx. Jedoch konnten Paket Abhängigkeiten zum jetzigen Zeitpunkt nicht aufgelöst werden und somit nicht getestet werden.

- OpenJDK standard JDK with javafx included ( [http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html))

## Testumgebung (Hardware &amp; Betriebssystem):

Operating System:  Windows 10 Education Professional

CPU Type:  2x Intel Pentium III Xeon, 2666 MHz

Video Adapter:         NVIDIA GeForce GTX 260

Physical Memory: 4095 MB DDR2

Disk Drive:  Samsung SSD 840 Series ATA Device  (111 GB, IDE)

Audio Adapter:   High Definition Audio Controller [NoDB]





## Betriebssysteme:

- [Ubuntu 16.04 LTS 32-Bit (Deutsch)](#ubuntu-16-04-lts-32-bit-deutsch)
- [Ubuntu 16.04 LTS 64-Bit](#ubuntu-16-04-lts-64-bit-englisch)
- [Ubuntu 16.04 LTS 64-Bit mit OpenJDK OpenJFK](#ubuntu-14-04-lts-64-bit-englisch-openjdk-openjfx)
- [Ubuntu 14.04 LTS 32-Bit](#ubuntu-14-04-lts-32-bit-englisch)
- [Ubuntu 14.04 LTS 64-Bit](#ubuntu-14-04-lts-64-bit-englisch)
- [Fedora 23 32-Bit](#fedora-23-32-bit-englisch)
- [Fedora 23 64-Bit](#Fedora 23 64-Bit (Englisch))
- [Fedora 23 64-Bit (Deutsch)](#fedora-23-64-bit-deutsch)
- [Debian Jessie (8) 32-Bit](#debian-jessie-8-32-bit)
- [Debian Jessie (8) 64-Bit](#debian-jessie-8-64-bit)
- [CentOS 6 32-Bit](#centos-6-32-bit)
- [CentOS 6 64-Bit](#centos-6-64-bit)
- [CentOS 7 64-Bit](#centos-7-64-bit)
- [Windows 10 64-Bit](#windows-10-64-bit-englisch)
- [Mac OS 10](#mac-os-10)

## Ergebnisse:

### CLI

CLI ([Command line interaction](http://jabref.sourceforge.net/help/CommandLine.php)) hat auf jedem Betriebssystem funktioniert.
Getestet wurde ein bib-import und die Hilfe Funktion über die Kommandozeilen-Befehle:
"java -jar JaBRef-3.6-JavaFX.jar -h"
"java -jar JaBRef-3.6-JavaFX.jar -i mybib.bib"

### Legende:

Aktion   – Getestetes Fenster

Dargest.  – Lies sich der Dialog öffnen?

Bemerkung  – Besondere Veränderungen

### Ubuntu 16 04 LTS 32 Bit Deutsch

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | Pinselbild wird nicht angezeigt. Stattdessen &quot;[]&quot; |
| Mathscinet | Ja | - |
| Groups rework | Ja | Statt dem Rechteckbild wird bei einigen Java Gruppe ein chinesisches Zeichen angezeigt. Journal und Keywords haben nur einen rechten Winkel. [Siehe Anhang](https://github.com/bruehldev/JabRef---Javafx-production-test/blob/master/JavaFXProduktionstest%20Anhang/Ubuntu%2016.04%2032-Bit%20Deutsch%20Groups%20rework.JPG) |
| Journal abbreviations | Nein | Kein Feedback. |
**Installation &amp; Ausführung:**
1.	sudo add-apt-repository ppa:webupd8team/java
2.	sudo apt-get update
3.	sudo apt-get install oracle-java8-installer
4.	java –jar JabRef-3.6-JavaFX.jar

**Java Version**
Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) Client  VM (build 25.101-b13, mixed mode)

### Ubuntu 16 04 LTS 64 Bit Englisch

Da dort alles optimal angezeigt wurde, habe ich andere zusätzlich andere JDK ohne Erweiterungen ausprobiert.

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Oracle JDK 6 or 7 | Error: Could not find or load main class net.sf.jabref.JabRefMain |
| OpenJDK 8 (Default)Not Oracle | Error: Could not find or load main class net.sf.jabref.JabRefMain |
| Installation &amp; Ausführung |
1. sudo add-apt-repository ppa:webupd8team/java
2. sudo apt-get update
3. sudo apt-get install oracle-java8-installer
4. java –jar JabRef-3.6-JavaFX.jar
 |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode) |

### Ubuntu 16 04 LTS 64 Bit Englisch OpenJDK

[AWT-EventQueue-0] WARN: net.sf.jabref.JabRefGUI – There seem to be problems with OPENJDK and the default GTK Look&amp;Feel. Using Metal L&amp;F instead. Change to another L&amp;F with caution.

| Error Console | Ja | - |
| --- | --- | --- |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | Neue Zeichen (Siehe Anhang) |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. sudo apt-get install openjdk-8-jdk
2. sudo apt-get install openjfx
 |
| Java Version | Openjdk version &quot;1.8.0\_91&quot;OpenJDK Runtime Environment (build 1.8.0\_91-8u91-8u91-b14-3ubuntu1~16.04.1-b14)OpenJDK 64-Bit Server VM (build 25.91-b14, mixed mode) |



### Ubuntu 14 04 LTS 32 Bit Englisch

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. sudo add-apt-repository ppa:webupd8team/java
2. sudo apt-get update
3. sudo apt-get install oracle-java8-installer
4. java –jar JabRef-3.6-JavaFX.jar
 |
| Java Version | Java version &quot;1.8.0\_92&quot;Java(TM) SE Runtime Environment (build 1.8.0\_92-b14)Java HotSpot(TM) Client VM (build 25.92-b14, mixed mode) |

### Ubuntu 14 04 LTS 64 Bit Englisch

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | Bei kleinerer Bildschirmauflösung wird nicht das ganze Fenter angezeigt, stattdessen muss gescrollt werden, obwohl es passen würde. |
| Journal abbreviations | Ja |
1. Versuch: Dialog erscheint oben links-&gt;Abstrurz von JabRef
2. Versuch: Neustart-&gt;Keine Probleme
3. Versuch: Keine Probleme
 |
| Installation &amp; Ausführung | [https://wiki.ubuntuusers.de/Java/Installation/Oracle\_Java/Java\_8/](https://wiki.ubuntuusers.de/Java/Installation/Oracle_Java/Java_8/)Download, Alternativen-System eingerichtet &amp; konfiguriert.  |
| Java Version | Java version &quot;1.8.0\_92&quot;Java(TM) SE Runtime Environment (build 1.8.0\_92-b14)Java HotSpot(TM) 64-Bit Server VM (build 25.92-b14, mixed mode) |

### Ubuntu 14 04 LTS 64 Bit Englisch OpenJDK OpenJFX

Wird nicht unterstützt und konnte somit nicht ausfeführt werden.

### Fedora 23 32 Bit Englisch

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | Pinselbild wird nicht angezeigt. Stattdessen &quot;[]&quot; |
| Mathscinet | Ja | - |
| Groups rework | Ja | Statt dem Rechteckbild wird bei einigen Java Gruppe ein chinesisches Zeichen angezeigt. Journal und Keywords haben nur einen rechten Winkel. Siehe Anhang |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Download Oracle JDK (i586)
2. Installieren mit rpm -ivh jdk-8u101-linux-x64.rpm
3. Upgraden mit rpm -Uvh jdk-8u101-linux-x64.rpm
4. alternatives --config java (2)
5. java –jar JaBRef
  |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM)Server VM (build 25.101-b13, mixed mode) |

### Fedora 23 64 Bit Englisch

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Download Oracle JDK
2. Installieren mit rpm -ivh jdk-8u101-linux-x64.rpm
3. Upgraden mitrpm -Uvh jdk-8u101-linux-x64.rpm
4. alternatives --config java (2)
5. java –jar JaBRef
  |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode) |

### Fedora 23 64 Bit Deutsch

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Nein | Kein Feedback |
| Installation &amp; Ausführung |
1. Download Oracle JDK
2. Installieren mit rpm -ivh jdk-8u101-linux-x64.rpm
3. Upgraden mitrpm -Uvh jdk-8u101-linux-x64.rpm
4. alternatives --config java (2)
5. java –jar JaBRef
  |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode) |

### Debian Jessie 8 32 Bit

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Anleitung: [https://wiki.debian.org/JavaPackage](https://wiki.debian.org/JavaPackage)
2. Java –jar JabRef
 |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) Client VM (build 25.101-b13, mixed mode) |

### Debian Jessie 8 64 Bit

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Anleitung: [https://wiki.debian.org/JavaPackage](https://wiki.debian.org/JavaPackage)
2. Java –jar JabRef
 |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode) |
| OpenJDK(OpenJFX wird nicht unterstützt)Ice Tea | Exception in thread &quot;main&quot; java.lang.UnsupportedClassVersionError:  net/s=f/jabref/JabRefMain :   Unsupported major.minor version 52.0   at java.lang.ClassLoader.defineClass1(Native Method   at java.lang.ClassLoader.defineClass(ClassLoader.java:803) |

### CentOS 6 32 Bit

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | Statt dem Rechteckbild wird bei einigen Java Gruppe ein chinesisches Zeichen angezeigt. Journal und Keywords haben nur einen rechten Winkel. Siehe Anhang |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Heruntergeladen von [oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
2. sudo yum localinstall jre-8u101-linux- i586.rpm
  |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM)Client VM (build 25.101-b13, mixed mode) |

### CentOS 6 64 Bit

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Heruntergeladen von [oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
2. sudo yum localinstall jre-8u101-linux-x64.rpm
  |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode) |

### CentOS 7 64 Bit

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Heruntergeladen von [oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
2. sudo yum localinstall jre-8u101-linux-x64.rpm
  |
| Java Version | Java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode) |

### Windows 10 64 Bit Englisch

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Heruntergeladen von [oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
2. Installations Wizzard ausgeführt
3. Jar ausgeführt
 |
| Java Version | java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode) |

### Mac OS 10

| **Aktion** | **Dargest.** | **Bemerkung** |
| --- | --- | --- |
| Error Console | Ja | - |
| Aboutdialog | Ja | - |
| Customize Key | Ja | - |
| Mathscinet | Ja | - |
| Groups rework | Ja | - |
| Journal abbreviations | Ja | - |
| Installation &amp; Ausführung |
1. Dmg heruntergeladen von [oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
2. Installations Wizzard ausgeführt Jar ausgeführt
 |
| Java Version | java version &quot;1.8.0\_101&quot;Java(TM) SE Runtime Environment (build 1.8.0\_101-b13)Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode) |

## Generelle Anmerkungen:

- Aus JavaFX Fenstern kann Text nicht ausgewählt und kopiert werden.
- Unter den Betriebsystemen Ubuntu 16.04 und Fedora als **32 Bit Systemen** ist die Anzeige von Bildern innerhalb von Groupsrework und Customoize Hotkey fehlerhaft.
- Unter CentOS 32 Bit ist nur der Groupsrework Dialog fehlerhaft.
- In **deutscher Sprache** eingestellt wird der Journal abbreviations nicht angezeigt.
- Die Bilder von Gruppen des Groupsrework werden abhängig vom Look&amp;Feel anders angezeigt (meist fehlerhaft).
