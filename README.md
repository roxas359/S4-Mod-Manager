# S4 Mod-Manager

Modpakete für **Die Siedler 4 History Edition** mit **Settlers United** aktivieren, anwenden und jederzeit wieder auf Original zurücksetzen.

## ⬇ Download

### **[⬇ S4-Mod-Manager.exe herunterladen (neueste Version)](https://github.com/roxas359/S4-Mod-Manager/releases/latest/download/S4-Mod-Manager.exe)**

Der Link lädt immer direkt die neueste `S4-Mod-Manager.exe`. Änderungen und Prüfsummen aller Versionen: [Releases](https://github.com/roxas359/S4-Mod-Manager/releases).

Spätere Updates holt der Mod-Manager selbst: **☰ Optionen → Nach Updates suchen…** – oder von Hand über **☰ Optionen → Neueste Version von GitHub laden** (bzw. den Link oben): Mod-Manager schließen, alte EXE durch die neue ersetzen, neu starten.

## 🔍 Updates – was genau passiert

- Der Mod-Manager geht **nur** ins Internet, wenn du **Nach Updates suchen…** klickst. Es gibt keine automatische Abfrage beim Start und kein Senden von Daten.
- Er fragt ausschließlich **dieses Repository** ab (`api.github.com/repos/roxas359/S4-Mod-Manager/releases/latest`) und lädt nur die Datei `S4-Mod-Manager.exe` des neuesten Releases.
- **Vor** dem Download zeigt er Version, Datum, Größe, die **SHA-256-Prüfsumme** und die Release-Notes, dazu einen Knopf **„Auf GitHub ansehen“**. Ohne deinen Klick auf *Herunterladen* passiert nichts.
- Nach dem Download prüft er Größe, EXE-Kopf und SHA-256. Passt etwas nicht, wird nichts ersetzt.
- Die vorige Version bleibt als `S4-Mod-Manager (Vorversion).exe` im Ordner. Jedes Update wird in `MODPACKS\_protokoll.log` eingetragen (von/nach, Prüfsumme, Quelle).

**Selbst nachprüfen:** Jedes Release enthält `S4-Mod-Manager.exe.sha256`. In der Eingabeaufforderung im EXE-Ordner:
```
certutil -hashfile S4-Mod-Manager.exe SHA256
```
Die angezeigte Zahl muss mit der aus der `.sha256`-Datei des Releases übereinstimmen. Alle bisherigen Versionen mit ihren Änderungen: **[Releases](https://github.com/roxas359/S4-Mod-Manager/releases)**.

## So geht's

1. `S4-Mod-Manager.exe` in einen eigenen Ordner legen, daneben einen Ordner `MODPACKS` mit den Paketen, die du bekommen hast:
   ```
   S4 Mod-Manager\
     EXE\S4-Mod-Manager.exe
     MODPACKS\<Paket>
   ```
2. Spiel und Settlers-United-Launcher schließen.
3. Im SU-Launcher die Version **„Lokale Dateien (nur Test)“** wählen – sonst setzt SU die Änderungen beim Start zurück.
4. Mod-Manager starten (fragt nach Adminrechten, weil er in `C:\Program Files\Settlers United` schreibt).
   Beim **ersten Start** legt er eine Originalsicherung an – das muss auf einem **unveränderten** Spiel passieren.
5. Paket links wählen → **Aktivieren →** → **ANWENDEN**. Zurück zum Original: **Alles Original**.

**Mehrspieler:** Alle brauchen dasselbe Paket. Der **MP-Code** oben im Fenster muss bei allen gleich sein (der *Zustands-Code* enthält zusätzlich Grafik/Sounds und darf abweichen). Das Spiel für den Mehrspieler immer über den **SU-Launcher** starten.

**Virenschutz:** Windows Defender meldet die EXE oder die `version.dll` eines Pakets manchmal fälschlich.
Hilfe: **☰ Optionen → Virenschutz-Fehlalarm beheben…**

Probleme nach einem Absturz/Desync: **☰ Optionen → Bug-Report kopieren** und im Discord einfügen. Der Bericht enthält Spiel-/SU-/Mod-Manager-Logs, Windows- und HD-Patch-Absturzberichte und – falls vorhanden – ein Absturzabbild als zweite Datei. Windows-Benutzer-/PC-Name und SU-Kontodaten (E-Mail, Token) werden vorher entfernt; die Datei heißt nach deinem SU-Kontonamen. Damit es Absturzabbilder gibt, schaltet der Mod-Manager dafür einmalig die Windows-Einstellung *LocalDumps* für `S4_Main.exe` ein.
