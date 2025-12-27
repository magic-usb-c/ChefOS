# ChefOS – Projektdefinition

## 1. Projektziel
Ich entwickle ein eigenes Linux-Betriebssystem („ChefOS“) auf Basis von
**Ubuntu Server 24.04 LTS (minimized)**.

Das Ziel ist ein **schlankes, bewusst aufgebautes Desktop-System**, das ich
vollständig verstehe und kontrolliere.

Am Ende soll daraus eine **eigene installierbare ISO** entstehen, die:
- vorkonfigurierte Apps und System-Settings enthält
- **keine persönlichen Benutzer** mitbringt
- beim Installieren (wie bei Ubuntu üblich) Benutzer und gewisse Optionen abfragt
- nach der Installation als **saubere Basis** dient

---

## 2. Hardware & Rahmenbedingungen
- Gerät: **Dell Latitude 5411**
- Boot-Modus: **UEFI**
- Secure Boot: **initial deaktiviert**
- Speicher: **eine einzelne SSD**
- Kein Dual-Boot, kein paralleles Windows auf dieser Maschine

---

## 3. Basis-System
- Distribution: **Ubuntu Server 24.04 LTS**
- Installationsart: **Ubuntu Server (minimized)**
- Zustand nach Installation:
  - kein GUI
  - keine Desktop-Umgebung
  - keine Snaps
  - kein unnötiger Server-Ballast
  - Login + Shell, alles Weitere manuell

---

## 4. Desktop- & Technik-Ziele
- Grafik-Stack: **Wayland**
- Compositor / WM: **Hyprland**
- Kein GNOME oder KDE als Basis
- Fokus auf:
  - Performance
  - saubere Konfiguration
  - Keyboard-Workflows
  - minimalen Ballast

Optik:
- clean
- flüssig
- animiert
- technisch / terminal-orientiert (eDEX-UI-ähnliche Anmutung)

---

## 5. Vorgehensweise
Das System wird schrittweise aufgebaut:

1. Minimalinstallation (CLI only)
2. Netzwerk bewusst konfigurieren
3. Grafik-Stack (Mesa, Wayland, Input)
4. Display-Manager
5. Hyprland
6. Basis-Apps
7. Optik, Animationen, Feinschliff

Jeder Schritt soll:
- erklärbar sein
- technisch begründet sein
- möglichst einfach rückgängig zu machen sein

---

## 6. Ziel: Eigene ISO
Sobald ChefOS stabil ist:
- Erstellung einer eigenen ISO
- Installation per Boot-Stick oder in VMs
- ChefOS dient danach als **Basis-System**, nicht als persönliches User-Setup

---

## 7. Anforderungen an die Unterstützung
- Antworten **kurz und übersichtlich**
- Jeder Schritt wird **kurz begründet** (Warum + Auswirkungen)
- Vorgehen **schrittweise als Tasks**:
  - immer nur **EIN Task**
  - darin alle wichtigen Punkte
  - erst nach Ausführung und Rückfragen folgt der nächste Task
- Fokus auf **Verständnis**, nicht auf „schnell fertig“

Wenn etwas fehlt oder kaputt ist, ist das **gewollt** – alles wird bewusst ergänzt.

---

## 8. Entscheidungs- und Auswahlprinzip (verbindlich)

Bei allen Schritten im Projekt **ChefOS** gilt:

- Es werden **keine Pakete, Tools, Apps oder Services ungeprüft installiert**.
- Vor jeder Installation werden **geeignete Optionen vorgeschlagen und kurz verglichen**:
  - Zweck / Einsatzgebiet
  - grobe Vor- und Nachteile
  - Auswirkungen auf Minimalismus, Abhängigkeiten und Wartbarkeit
- Erst danach folgt **eine begründete Empfehlung**.
- Konkrete Installationsbefehle kommen **erst nach einer bewussten Entscheidung**.

Ziel dieses Prinzips:
- Technisches **Verständnis statt blindes Ausführen**
- **Bewusste Systemgestaltung** statt Convenience
- ChefOS soll **durchdrungen, nicht nur benutzt** werden

Erwartetes Antwortverhalten:
- Vorschläge in **kleinen, sinnvollen Auswahlsets** (typisch 2–4 Optionen)
- Sachliche Begründungen ohne Marketing-Sprache
- Hinweise, **was sinnvoll selbst nachzulesen oder zu vergleichen ist**
- Klare Trennung zwischen **Entscheidungsphase** und **Umsetzungs-Task**

Dieses Prinzip gilt **projektweit**, in **jedem Chat**, auch bei scheinbar kleinen Tools.

---

## 9. Projektweite Vorgaben & Pflege der Projektdefinition

Wenn ich neue Vorgaben formuliere, die **projektweit gelten sollen**:

- Gib mir **direkt den passenden Abschnitt** für diese Datei (`PROJECT.md`)
- Immer im **reinen Markdown-Format**, zum Copy-Paste geeignet
- **Nur bei inhaltlich sinnvollen Änderungen** an der Projektdefinition

Zusätzlich:
- Gib mir bei solchen Änderungen **den passenden Git-Befehl** an,
  damit das Repository sauber und nachvollziehbar aktualisiert wird

Ziel:
- Die `PROJECT.md` ist die **Single Source of Truth**
- Projektentscheidungen sind **versioniert und nachvollziehbar**
- Neue Chats können sich jederzeit korrekt am Projekt ausrichten
