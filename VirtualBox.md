# Virtual Box

VirtualBox ist eine Open-Source-Virtualisierungssoftware, die von Oracle entwickelt wird. Sie ermöglicht es
Benutzern, virtuelle Maschinen (VMs) auf ihren Computern auszuführen. VirtualBox ist plattformübergreifend
und unterstützt verschiedene Host-Betriebssysteme wie Windows, macOS, Linux und Solaris. Mit VirtualBox
können Sie Gastbetriebssysteme auf Ihrem Computer ausführen, ohne Ihr Hauptbetriebssystem zu ändern
oder zu beeinträchtigen. Verwendungszwecke und Merkmale von VirtualBox sind:

1. Isolierung und Testen: VirtualBox ermöglicht es Benutzern, verschiedene Betriebssysteme, einschließlich
verschiedener Versionen von Windows, Linux, macOS und mehr, in virtuellen Maschinen zu installieren und
auszuführen. Dies ist besonders nützlich für Entwickler und Tester, um Software in verschiedenen
Umgebungen zu testen, ohne physische Hardware zu benötigen.

2. Entwicklung und Debugging: Entwickler können VirtualBox nutzen, um Entwicklungsumgebungen für
verschiedene Plattformen zu erstellen und Anwendungen in isolierten Umgebungen zu entwickeln und zu
debuggen. Dies ermöglicht die problemlose Anpassung an verschiedene Zielplattformen.

3. Sicherheit: Virtuelle Maschinen können in isolierten Containern betrieben werden, wodurch die Sicherheit
erhöht wird. Wenn ein Gastbetriebssystem kompromittiert wird, hat dies in der Regel keinen Einfluss auf das
Host-Betriebssystem.

4. Ressourcenmanagement: VirtualBox bietet fortschrittliche Funktionen zur Steuerung und Überwachung
von Ressourcen wie CPU, Arbeitsspeicher und Netzwerkverbindungen für virtuelle Maschinen.

5. Snapshots und Cloning: VirtualBox ermöglicht das Erstellen von Snapshots, die den Zustand einer VM zu
einem bestimmten Zeitpunkt erfassen. Dies erleichtert das Sichern und Wiederherstellen von VMs. Sie können
auch VMs klonen, um schnell Kopien zu erstellen.

6. Zusätzliche Funktionen: VirtualBox bietet Unterstützung für das gemeinsame Nutzen von Ordnern
zwischen dem Host und den Gastsystemen, das Einbinden von virtuellen Festplatten und die Unterstützung
für USB-Geräte in VMs.

#### Virtual Disk Image

Ein Virtual Disk Image (virtuelles Festplattenabbild) ist eine Datei, die den Inhalt einer virtuellen Festplatte
oder eines virtuellen Speichergeräts darstellt. Diese Dateien werden häufig in Virtualisierungsumgebungen
verwendet, um das Betriebssystem, die Anwendungen und die Daten einer virtuellen Maschine (VM) oder
eines virtuellen Speichergeräts zu speichern.
Ein Virtual Disk Image kann verschiedene Formate haben, je nach der Virtualisierungssoftware, die verwendet
wird. VirtualBox verwendet das VDI-Format.
Dynamically Allocated ermöglicht, dass der Speicherplatz auf der physischen Festplatte erst dann tatsächlich
belegt wird, wenn Daten auf der virtuellen Festplatte gespeichert werden. Mit anderen Worten, die virtuelle
Festplatte wächst nach Bedarf und verwendet nur so viel Speicherplatz auf der physischen Festplatte, wie
tatsächlich erforderlich ist.


### BIOS (Basic Input/Output System):

Das BIOS ist ein grundlegendes, fest in der Computerhardware verankertes System. Es dient dazu, den
Computer beim Starten zu initialisieren und grundlegende Hardwarefunktionen zu aktivieren. Das BIOS ist in
einem nicht-flüchtigen Speicherchip auf dem Motherboard eines Computers gespeichert und enthält
grundlegende Informationen zur Hardwarekonfiguration, wie CPU, RAM, Festplatten und Peripheriegeräte. Es
ermöglicht auch den Startvorgang, indem es den Computer anweist, von einem bestimmten Gerät,
normalerweise einer Festplatte oder einem USB-Laufwerk, zu booten. Dazu ist der Master Boot Record (MBR)
auf startfähigen Datenträgern notwendig und besteht aus zwei Teilen:
einem Startprogramm (englisch Bootstrap Code) – jenes Programm im Bootsektor, das im
Chainloading-Prinzip den Bootloader eines Betriebssystems auf einer der Partitionen startet.
einer Partitionstabelle – in diesem Zusammenhang wird auch oft von einem Partitionssektor (englisch
partition sector) gesprochen. Obwohl das BIOS in der Vergangenheit weit verbreitet war, wurde es in
den letzten Jahren zunehmend durch das modernere UEFI ersetzt.

### UEFI (Unified Extensible Firmware Interface):

UEFI ist ein moderneres und leistungsfähigeres Firmware-Interface, das das BIOS in vielen aktuellen
Computern ersetzt hat. Im Gegensatz zum textbasierten BIOS bietet UEFI eine grafische Benutzeroberfläche
und erweiterte Funktionen. Es können große Festplatten mit über 2 TB mit einer im Rahmen von UEFI
eingeführten GUID-Partitionstabelle (GPT) verwendet werden. GPT ist dabei der Nachfolger der
Partitionstabelle des Master Boot Record.

### Partitionierung (Debian)
Die Partitionierung eines Debian-Servers hängt von den spezifischen Anforderungen und dem
Verwendungszweck des Servers ab. Hier sind einige Beispiele für eine mögliche Partitionierung und eine
Erklärung der einzelnen Partitionstypen:
##### 1. / (Root-Partition):

Die Root-Partition ist die wichtigste Partition auf einem Debian-Server. Hier wird das
Betriebssystem installiert, und sie enthält alle Systemdateien und Programme. Sie sollte ausreichend
Speicherplatz haben, um das Betriebssystem, die Softwareanwendungen und temporäre Dateien
aufzunehmen. Eine typische Größe für die Root-Partition beträgt 20-30 GB.
##### 2. /boot (Boot-Partition):

Die /boot-Partition enthält die für den Bootvorgang des Servers erforderlichen
Dateien, wie den Linux-Kernel und das Bootloader-Programm (z. B. GRUB). Diese Partition ist normalerweise
klein und benötigt in der Regel nur einige hundert Megabyte Speicherplatz. Sie sollte nicht zu klein sein, da
sonst Probleme beim Aktualisieren des Kernels auftreten können.
#### 3. /home (Home-Partition):

Die /home-Partition ist der Speicherort für Benutzerdaten, Dateien und
Verzeichnisse. Sie kann auf einer eigenen Partition erstellt werden, um die Benutzerdaten von anderen
Systemdateien zu trennen. Die Größe hängt von der erwarteten Menge an Benutzerdaten ab, sollte aber
ausreichend Platz bieten, um Benutzerdateien und -verzeichnisse zu speichern.
#### 4. /var (Variable-Partition):

Die /var-Partition speichert variable Daten, darunter Log-Dateien,
Datenbankdateien und temporäre Dateien. Diese Partition kann erheblichen Speicherplatz benötigen, je
nachdem, wie intensiv der Server verwendet wird. Sie sollte groß genug sein, um die für den Serverbetrieb
benötigten Daten zu speichern.

#### 5. /tmp (Temporary-Partition):

Die /tmp-Partition ist für temporäre Dateien vorgesehen, die während des
Serverbetriebs erstellt werden. Sie sollte relativ klein sein, um sicherzustellen, dass der Speicherplatz nicht
übermäßig beansprucht wird. Einige Sicherheitsrichtlinien empfehlen sogar, die /tmp-Partition in den RAM zu
mounten, um die Geschwindigkeit zu erhöhen und temporäre Dateien bei jedem Neustart zu löschen.
#### 6. Swap-Partition:

Die Swap-Partition ist der Bereich auf der Festplatte, der als virtueller Speicher verwendet
wird, wenn der physische RAM des Servers erschöpft ist. Die Größe der Swap-Partition hängt von der Menge
des physischen RAM ab, kann jedoch in der Regel doppelt so groß sein wie der RAM. Swap wird verwendet,
um den Serverbetrieb bei hohem Arbeitsspeicherverbrauch aufrechtzuerhalten.
#### 7. /usr (User-Partition):

Die /usr-Partition enthält die meisten Programme und Bibliotheken auf dem System.
Sie sollte ausreichend Platz bieten, um Programme und Anwendungen zu installieren. Eine typische Größe für
/usr beträgt mehrere Gigabyte.