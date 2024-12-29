📘 Ansible Playbook: Server-Wartung und Aktualisierung

📑 Übersicht

Dieses Ansible-Playbook automatisiert die Wartung und Aktualisierung von Linux-Servern. Es stellt sicher, dass die Paketlisten aktualisiert werden, wichtige Softwarepakete installiert sind und Kernel-Updates bei Bedarf durch einen Neustart des Servers abgeschlossen werden.

⚙️ Funktionen des Playbooks

Paketlisten aktualisieren: Aktualisiert den Paketmanager-Cache (APT).

Systempakete aktualisieren: Führt ein vollständiges Upgrade der installierten Pakete durch.

Software installieren: Installiert grundlegende Softwarepakete (z.B. duf, needrestart, htop).

Kernel-Update prüfen: Überprüft, ob ein neuer Kernel installiert wurde.

Server-Neustart: Startet den Server bei Bedarf neu.

Neustart überwachen: Stellt sicher, dass der Server nach dem Neustart wieder verfügbar ist.

Systemstatus prüfen: Zeigt die Betriebszeit (uptime) des Servers an.

🚀 Verwendung des Playbooks

Voraussetzungen

Ansible ist auf dem Steuerrechner installiert.

SSH-Zugriff auf die Zielserver ist konfiguriert.

Eine Ansible-Inventardatei mit den Zielservern ist vorhanden.

Playbook ausführen

ansible-playbook -i inventory.ini playbook.yml

-i inventory.ini: Gibt die Inventardatei an.

playbook.yml: Der Dateiname des Playbooks.

Beispiel-Inventardatei (inventory.ini)

[all]
server1.example.com
server2.example.com

Debug-Informationen anzeigen

Um Debug-Informationen anzuzeigen, füge die Option -v hinzu:

ansible-playbook -i inventory.ini playbook.yml -v

🛡️ Wichtige Hinweise

Führe das Playbook zuerst auf einem Testsystem aus.

Stelle sicher, dass vor dem Neustart offene Verbindungen und laufende Dienste gesichert sind.

