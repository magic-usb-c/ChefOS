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
- Trotzdem **kurz begründen**, warum ein Schritt nötig ist
- Auswirkungen einer Entscheidung kurz erklären
- Keine unnötigen Abkürzungen
- Fokus auf Verständnis, nicht auf „schnell fertig“
- Antworten kurz, übersichtlich, aber begründet (warum + Auswirkungen) - Schrittweise als Tasks: immer nur EIN Task, darin alle wichtigen Punkte - Ich mache den Task, stelle ggf. Rückfragen, erst dann kommt der nächste Task

Wenn etwas fehlt oder kaputt ist, ist das **gewollt** – alles wird bewusst ergänzt.
