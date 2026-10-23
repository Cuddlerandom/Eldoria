# ELDORIA – GAME DESIGN DOCUMENT
Version: 0.3 (Planungsstand 23.10.2026)
Status: Lebendes Designdokument. Änderungen nur nach Designentscheidung.

## 1. Vision
Eldoria ist ein eigenständiges, von klassischen Fantasy-MMORPGs wie World of Warcraft Classic inspiriertes 2D-Rollenspiel. Ziel ist das langsame, befriedigende Erkunden einer zusammenhängend wirkenden Fantasywelt mit Quests, Kämpfen, Klassenentwicklung, Loot und Dungeons. Keine Übernahme fremder Namen, Grafiken, Karten oder geschützter Inhalte. Zunächst Singleplayer, Multiplayer allenfalls später.

## 2. Zielplattform und Technik
- Primär iPhone Safari, Touch-first; Browser-Spiel über GitHub Pages.
- Repository: Cuddlerandom/Eldoria
- Spieladresse: https://cuddlerandom.github.io/Eldoria/
- Ziel: flüssige 60 FPS auf dem iPhone.
- Aktuelle Implementierung: HTML5 Canvas mit Vanilla JavaScript in index.html; Phaser ist **nicht** integriert.
- Virtueller Joystick links, Zielwahl und Fähigkeiten rechts; derzeit Querformat.
- Lokaler Spielstand über localStorage (vorläufig).
- Gebiete perspektivisch als separate Zonen mit Übergängen/Ladewechseln.

## 3. Verbindlicher Grafikstil
- Moderne, detaillierte 2D-Fantasy-Pixel-Art.
- Perspektive **A: direkt von oben (90° Vogelperspektive)**, nicht schräg.
- Ausgangsbasis für Umgebung: 32×32-Tiles (noch nicht als echte Tiles implementiert).
- Gut erkennbare Charaktere, Gegner, Rüstung, Waffen und Fähigkeiten.
- Mobile Performance hat Priorität.
- Derzeitige Welt/Charaktere sind programmatisch gezeichnete Platzhalter.

## 4. Welt und Völker
- Zwei rivalisierende Fraktionen mit je vier spielbaren Völkern (Namen und Zuordnung noch zu designen).
- Jedes Volk soll langfristig ein eigenes Startgebiet haben.
- **Entscheidung A: Dämmerhain ist ausschliesslich das Menschen-Startgebiet.**
- Grosse, erkundbare Zonen mit Levelbereichen, Quests, Gegnern, Städten und später Dungeons.

## 5. Menschen-Startgebiet: Dämmerhain
- Ausgangsort: **Kloster Silberquell**.
- Vorbild für den Spielfluss: klassische Startgebiete mit sicherem Klosterhof, Questgebern, kurzen Erkundungswegen und steigender Gefahr.
- Vorgesehener Levelbereich: 1–5, späterer Ausbau bis etwa Level 10.
- Teilgebiete: Klosterhof/Trainingsbereich, Waldwege und Wolfslichtung, Vorratsroute, Plündererlager, Ausgang zur Folgezone.
- Wichtige Figuren: Hauptmann Arven, Versorgerin Mira, Wache Taron.
- Eine erste schematische Karte wurde in V0.2 implementiert. Das ist noch keine fertige Pixel-Art-Map.

## 6. Questsystem – Entscheidung A
- **Mehrere Quests gleichzeitig annehmen und frei in beliebiger Reihenfolge erledigen**, wie in klassischen MMORPGs.
- Questlog mit allen aktiven Quests und individuellen Fortschritten.
- Gelbes ! für verfügbare Quests, ? für abgabebereite Quests.
- Questannahme über NPC-Dialog, Ziele erfüllen, Rückkehr und Belohnung.
- Questreihen dürfen Voraussetzungen und Freischaltungen besitzen.
- Geplante und in V0.3 erstmals programmierte Aufträge:
  1. **Wölfe vor den Toren** – 5 Wölfe besiegen; Hauptmann Arven; 100 XP Questbelohnung.
  2. **Verlorene Vorräte** – 4 Kisten sammeln; Versorgerin Mira; 150 XP.
  3. **Die Plünderer** – 6 Plünderer besiegen; Wache Taron; 150 XP.
  4. **Gefahr aus dem Wald** – Plündererhauptmann besiegen; nach „Die Plünderer“; 250 XP.
- Weitere Quests, Dialogtiefe und Belohnungen später ausbauen.

## 7. Kampf
- Klassisches Tab-/Tap-Target-Konzept: Gegner auswählen, automatische Standardangriffe in Reichweite, aktive Fähigkeiten manuell auslösen.
- Angriffsreichweite, Abklingzeiten, Aggro und Verfolgung.
- Erste spielbare Klasse: Krieger mit Schwertangriff.
- Gegner können Spieler angreifen; Tod führt vorläufig zum Respawn am Startpunkt.
- Später: klassenspezifische Ressourcen, vielfältige Fähigkeiten, Statuswerte, Ausrüstung und Gegnerverhalten.
- Aktuelle V0.3-Gegner: Wölfe, Plünderer, Plündererhauptmann (grafische Platzhalter).

## 8. Klassen, Level und Talente
- Geplante neun klassische Fantasy-Archetypen: Krieger, Paladin, Jäger, Schurke, Magier, Hexenmeister, Priester, Druide, Schamane. Originale Eldoria-Bezeichnungen können später festgelegt werden.
- Charaktererstellung mit Volk und Klasse ist geplant, nicht implementiert.
- Langsames Leveln von 1 bis 60 mit spürbaren Meilensteinen.
- Drei Talentbäume je Klasse.
- Ab Level 10 ein Talentpunkt pro Level; maximal 51 Punkte auf Level 60.
- Mehrstufige Talente, Voraussetzungen und besondere Schlüsseltalente geplant.
- Balance und Details noch nicht final definiert.

## 9. Loot, Progression und Inhalte (geplant)
- Klassische RPG-Ausrüstung, Waffen, Rüstungen, Gegenstandsqualität und Upgrades.
- Quests, normale Gegner, Elitegegner, Bosse, Dungeons.
- Wirtschaft, Händler, Inventar und Charakterwerte müssen noch spezifiziert werden.
- Zunächst ein solides Singleplayer-RPG; Multiplayer ist keine Voraussetzung für die frühen Versionen.

## 10. UI und Bedienung
- Mobile-first, möglichst gut lesbare HUD-Elemente und Touch-Ziele.
- Links virtueller Joystick; rechts Ziel- und Fähigkeitsbuttons.
- HP, Level, XP, Zielstatus, Questlog.
- Dialoge für NPCs und Questannahme/Abgabe.
- Langfristig weitere Menüs: Charakter, Inventar, Talente, Karte und Questlog.
- Querformat ist der aktuelle Prototyp-Standard.

## 11. Entwicklungsstand (nicht mit getesteter Freigabe verwechseln)
### V0.1 – vom Nutzer auf iPhone getestet
- Bewegung gut, Kampf gut, Performance flüssig.
- Einfache Welt, Krieger, Wölfe, Zielwahl, XP und Speicherung.

### V0.2 – vom Nutzer bestätigt
- Dämmerhain mit schematischem Kloster Silberquell und Hauptmann Arven.
- Erste Questannahme, Wolf-Kill-Fortschritt und XP-Abgabe funktionieren laut Nutzer.

### V0.3 – auf main implementiert, **noch nicht vom Nutzer getestet**
- Mehrere parallel laufende Quests, Questlog, zusätzliche Questgeber.
- Sammelkisten, Plünderer und Plündererhauptmann.
- Vor weiterer Feature-Entwicklung: auf iPhone testen und Fehler korrigieren.
- Insbesondere Quest-NPCs, Ziele, Boss-Freischaltung, Speicherstand und Bedienung prüfen.

## 12. Nächste Prioritäten
1. V0.3 auf iPhone testen und Fehler beheben.
2. Saubere Spielwelt mit richtigen Pixel-Art-Tiles, Kollisionssystem und lesbaren Wegen.
3. Besseres Questlog und Dialog-UI.
4. Inventar, Gegenstandsbelohnungen und Händler.
5. Weitere Startzonen, Klassen und Kampffähigkeiten.

## 13. Projektregeln
- Bestätigte Entscheidungen hier dokumentieren; unentschiedene Fragen als offen markieren.
- Keine Funktionen als getestet ausgeben, solange kein echter Test stattgefunden hat.
- Vor Änderungen bestehenden Code und Designentscheidungen prüfen.
- Spielstände möglichst kompatibel halten und bei Änderungen Migration berücksichtigen.
- Eldoria nicht mit anderen Spieleprojekten verwechseln.
