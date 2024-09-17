# Einführung in das Thema Virtualisierung

Virtualisierung ist ein zentrales Konzept in der Informationstechnologie, das die Art und Weise, wie
Computerressourcen genutzt werden, revolutioniert hat. Sie ermöglicht es, physische Hardware-Ressourcen
auf effiziente Weise zu nutzen, indem sie virtuelle Umgebungen schafft, die unabhängig voneinander
betrieben werden können. Diese Technologie hat die Flexibilität, Skalierbarkeit, Sicherheit und Verwaltbarkeit
von IT-Infrastrukturen erheblich verbessert und spielt eine entscheidende Rolle in modernen Rechenzentren,
Cloud Computing und vielen anderen Bereichen der IT.

Im Wesentlichen geht es bei der Virtualisierung darum, die Trennung zwischen der physischen Hardware und
der darauf ausgeführten Software herzustellen. Dies geschieht durch die Erstellung virtueller Maschinen (VMs)
oder Container, die wie eigenständige Computer innerhalb des physischen Hosts agieren. Hier sind einige
Schlüsselkonzepte und Vorteile der Virtualisierung:

### 1. Ressourcenkonsolidierung:
Virtualisierung ermöglicht es, mehrere VMs auf einem einzelnen
physischen Server auszuführen. Dies führt zu einer besseren Auslastung der Hardware-Ressourcen, da
Server, die normalerweise unterausgelastet sind, effizient genutzt werden können.
### 2. Isolation:
Jede VM ist von den anderen isoliert, was bedeutet, dass sie unabhängig voneinander
betrieben werden können. Diese Isolation schützt vor Konflikten und Sicherheitsproblemen, da
Probleme in einer VM nicht auf andere übertragen werden.
### 3. Schnelle Bereitstellung:
Das Erstellen und Bereitstellen von VMs ist in der Regel schneller und
einfacher als der Kauf und die Konfiguration physischer Hardware. Dies erleichtert die Skalierbarkeit
und Anpassungsfähigkeit von IT-Infrastrukturen.
### 4. Migration und Disaster Recovery:
Virtualisierte Umgebungen ermöglichen die einfache Migration von
VMs zwischen physischen Hosts und bieten eine effiziente Lösung für Disaster-Recovery-Szenarien.
### 5. Test und Entwicklung:
Entwickler können virtuelle Umgebungen erstellen, um Softwareanwendungen
zu testen und zu entwickeln, ohne physische Hardware-Ressourcen zu beanspruchen.
### 6. Energieeffizienz:
Durch die Konsolidierung von VMs auf weniger physischen Servern kann Energie gespart werden, da weniger Hardware-Komponenten aktiv sein müssen.
Es gibt verschiedene Arten der Virtualisierung, darunter Hardwarevirtualisierung, bei der eine
Virtualisierungssoftware (Hypervisor) auf der physischen Hardware läuft und VMs verwaltet, und Container-
Virtualisierung, bei der Anwendungen und ihre Abhängigkeiten in Containern isoliert werden. Virtualisierung
beeinflusst wie Unternehmen IT-Ressourcen verwalten und bereitstellen. Diesee Aufgaben werden durch
Virtualisierung erheblich vereinfacht und optimiert.

## Hypervisor
Es gibt zwei Hauptarten von Hypervisoren, die in der Virtualisierungstechnologie verwendet werden: Typ-1-
Hypervisor (bare-metal) und Typ-2-Hypervisor (hosted). Jede dieser Hypervisor-Arten hat ihre eigenen Vor-
und Nachteile sowie Anwendungsfälle. Hier ist eine Übersicht über beide Typen:
#### 1. Typ-1-Hypervisor (Bare-Metal-Hypervisor):
Dieser Hypervisor wird direkt auf der physischen Hardware des Host-Systems installiert.
- Er arbeitet ohne ein Host-Betriebssystem und hat daher einen direkten Zugriff auf die Hardware-Ressourcen. -
Typ-1-Hypervisoren bieten in der Regel eine bessere Leistung und Skalierbarkeit als Typ-2-
Hypervisoren, da sie keine zusätzliche Software-Ebene (das Host-Betriebssystem) durchlaufen
müssen.
![Typ1 Hypervisor](/images/Hypervisor1.png)


- Beispiele für Typ-1-Hypervisoren sind VMware vSphere/ESXi, Microsoft Hyper-V (in einigen
Konfigurationen), Xen und KVM (Kernel-based Virtual Machine).
#### 2. Typ-2-Hypervisor (Hosted Hypervisor):
Dieser Hypervisor wird auf einem bereits vorhandenen Host-Betriebssystem installiert. - Er ist
einfacher einzurichten und bietet eine höhere Benutzerfreundlichkeit, da er auf einem normalen
Betriebssystem wie Windows, macOS oder Linux läuft.

- Typ-2-Hypervisoren sind oft nützlich für Entwicklung, Tests und Schulungen, da sie weniger komplex
sind und weniger Einfluss auf das Host-System haben.
- Sie können jedoch in Bezug auf Leistung und
Sicherheit weniger effizient sein, da sie durch das Host-Betriebssystem beschränkt sind
- Beispiele für Typ-2-Hypervisoren sind Oracle VirtualBox, VMware Workstation und Parallels Desktop.
Die Wahl zwischen Typ-1- und Typ-2-Hypervisoren hängt von den spezifischen Anforderungen und
dem Einsatzzweck ab. In Unternehmensumgebungen, in denen Leistung und Sicherheit von größter
Bedeutung sind, werden Typ-1-Hypervisoren häufig bevorzugt. Typ-2-Hypervisoren sind jedoch eine
gute Wahl für Desktop-Virtualisierung, Entwicklungsumgebungen oder Benutzer, die einfachere
Virtualisierungslösungen benötigen.

##### Beispiel für Typ-2-Hypervisoren:
1. Oracle VirtualBox: VirtualBox ist ein Open-Source-Typ-2-Hypervisor, der von Oracle entwickelt wird. Er
ist weit verbreitet, einfach zu installieren und bietet eine breite Palette von Funktionen. VirtualBox
unterstützt verschiedene Gastbetriebssysteme und ist sowohl für Windows, macOS als auch für Linux
verfügbar.
2. VMware Workstation: VMware Workstation ist ein kommerzieller Typ-2-Hypervisor, der von VMware
entwickelt wird. Er richtet sich an Entwickler, Tester und Power-User und bietet fortschrittliche
Funktionen und Leistungsoptimierungen. VMware Workstation ist für Windows und Linux verfügbar.
3. Parallels Desktop: Parallels Desktop ist eine kommerzielle Virtualisierungslösung für macOS. Es
ermöglicht Mac-Benutzern, Windows und andere Betriebssysteme in einer virtuellen Umgebung
auszuführen. Es ist bekannt für seine Benutzerfreundlichkeit und Integration mit dem Mac-
Betriebssystem.
4. QEMU: QEMU (Quick EMUlator) ist ein Open-Source-Emulator und Typ-2-Hypervisor, der für
verschiedene Gastbetriebssysteme und Architekturen geeignet ist. Es wird oft in Kombination mit dem
KVM-Hypervisor (Kernel-based Virtual Machine) verwendet, um eine leistungsstarke
Virtualisierungslösung für Linux-Systeme bereitzustellen. Diese Hypervisoren sind bei Anwendern
aufgrund ihrer Zuverlässigkeit, Benutzerfreundlichkeit und einer breiten Palette von Funktionen beliebt.
Paravirtualisierung und Vollvirtualisierung sind zwei verschiedene Ansätze zur Virtualisierung von
Hardware-Ressourcen, insbesondere von Prozessoren, in einer virtuellen Umgebung. Beide Ansätze
ermöglichen es, mehrere virtuelle Maschinen (VMs) auf einem einzelnen physischen Host auszuführen,
unterscheiden sich jedoch in ihrer Herangehensweise und ihren Anforderungen.


## Virtualisierungstechnologien
#### Vollvirtualisierung:
Die Vollvirtualisierung, auch bekannt als Hardwarevirtualisierung, zielt darauf ab, virtuelle
Maschinen (VMs) so zu erstellen, dass sie sich verhalten, als würden sie auf echter physischer Hardware laufen.
In diesem Ansatz wird ein Hypervisor (Virtual Machine Monitor) verwendet, der die Hardware abstrahiert und
die VMs so konfiguriert, dass sie die physische Hardware imitiert. Die VMs sind sich normalerweise nicht
bewusst, dass sie virtualisiert sind, da sie die Illusion haben, auf eigener Hardware zu laufen. Ein wichtiger
Aspekt der Vollvirtualisierung ist die Unterstützung nicht-modifizierter Gastbetriebssysteme. Dies bedeutet,
dass Sie in der Lage sind, herkömmliche Betriebssysteme ohne spezielle Anpassungen in VMs auszuführen.
Diese Art der Virtualisierung ist oft effizienter und bietet eine höhere Isolation zwischen den VMs, da sie nicht-
modifizierte Betriebssysteme in getrennten Umgebungen ausführt. Beispiele für
Vollvirtualisierungshypervisoren sind VMware vSphere/ESXi, Microsoft Hyper-V und Xen (in bestimmten
Konfigurationen).

#### Paravirtualisierung:
Die Paravirtualisierung ist eine Virtualisierungstechnik, bei der das Gastbetriebssystem speziell angepasst oder
"paravirtualisiert" wird, um in einer virtualisierten Umgebung zu laufen. Anders als bei der Vollvirtualisierung
sind sich die Gastbetriebssysteme bewusst, dass sie virtualisiert sind, und sie interagieren direkt mit dem
Hypervisor, um Ressourcen zuzuweisen und zu verwalten. Die Paravirtualisierung kann in bestimmten Fällen
die Leistung verbessern, da die Kommunikation zwischen dem Gastbetriebssystem und dem Hypervisor
optimiert werden kann. Allerdings erfordert die Paravirtualisierung in der Regel eine Anpassung des
Gastbetriebssystems, was bedeutet, dass Sie spezielle, für die Paravirtualisierung angepasste Versionen
verwenden müssen. Ein Beispiel für eine Paravirtualisierungslösung ist Xen, das sowohl in Vollvirtualisierung
als auch in Paravirtualisierung konfiguriert werden kann, je nach den Anforderungen und dem Betriebssystem
der VMs. Insgesamt hängt die Wahl zwischen Vollvirtualisierung und Paravirtualisierung von den spezifischen
Anforderungen, der Leistung und der Kompatibilität der verwendeten Betriebssysteme ab. Vollvirtualisierung
bietet in der Regel mehr Flexibilität, während Paravirtualisierung in bestimmten Fällen die Leistung verbessern
kann.