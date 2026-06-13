# SomeThink CRM – Releases

Öffentliche Release-Artefakte für die Auto-Update-Funktion von **SomeThink CRM**.
Der Quellcode liegt im privaten Repo `jpboehm/SomethinkCRM`.

👉 **Aktuelle Version herunterladen:** [Neuestes Release](https://github.com/jpboehm/SomethinkCRM-releases/releases/latest)

---

## Installation (macOS, Apple Silicon)

1. Im neuesten Release die Datei **`SomeThink-CRM-<Version>-arm64.dmg`** herunterladen.
2. DMG per Doppelklick öffnen und **SomeThink CRM** in den Ordner **„Programme"** ziehen.
3. App **einmalig freigeben** (siehe unten) – danach startet sie normal.

### Beim ersten Start: „Apple konnte nicht überprüfen …"

Die App ist gültig signiert, aber **nicht von Apple notarisiert**. macOS zeigt deshalb
beim ersten Start eine Sicherheitswarnung. Das ist normal und unbedenklich – die App
muss nur **einmal** manuell freigegeben werden. Wähle **einen** der beiden Wege:

#### Weg A – über die Systemeinstellungen (empfohlen)

1. App in „Programme" doppelklicken → Warnung erscheint → auf **„Fertig"** klicken.
2. **Systemeinstellungen → Datenschutz & Sicherheit** öffnen.
3. Nach unten zum Abschnitt **„Sicherheit"** scrollen. Dort steht:
   *„SomeThink CRM.app wurde blockiert…"* → Button **„Trotzdem öffnen"** klicken.
4. Mit Touch ID / Passwort bestätigen, dann im erneuten Dialog nochmals **„Trotzdem öffnen"**.

> Hinweis: Auf macOS 15 (Sequoia) und neuer funktioniert der frühere
> „Rechtsklick → Öffnen"-Trick **nicht mehr** – nutze den Weg über die Systemeinstellungen.

#### Weg B – Terminal (ein Befehl, am zuverlässigsten)

```bash
xattr -dr com.apple.quarantine "/Applications/SomeThink CRM.app"
```

Entfernt das Quarantäne-Flag; die App startet anschließend direkt ohne Dialog.

---

## Updates

Ab Version **3.0.2** aktualisiert sich die App **automatisch**: Sie meldet sich, sobald
ein neues Release verfügbar ist, und installiert es nach Bestätigung. Die manuelle
Freigabe von oben ist dann **nicht erneut** nötig.

> Wer noch eine ältere, manuell installierte Version nutzt, muss **einmalig** das
> aktuelle DMG von Hand installieren – danach läuft das Auto-Update.
