---
titel: Call-Tracking-Nummern im Profil schützen
typ: wissen
evidenz: gemischt — je Aussage einzeln ausgewiesen
verifiziert_am: 2026-08-27
naechste_pruefung: 2026-11-27
gilt_fuer: kanalservice-dach
owner: harun
status: entwurf
---

# Call-Tracking-Nummern im Profil schützen

## Kurzfassung

1. Google ersetzt Telefonnummern im Profil eigenmächtig, wenn im Netz überall eine andere Nummer steht. Eine Call-Tracking-Nummer ist genau so ein Fall.
2. Der Schaden ist unsichtbar: Die Anrufe kommen weiter an, werden aber nicht mehr erfasst. Der Kunde sieht weniger Leads aus Google, obwohl sich an der Sichtbarkeit nichts geändert hat.
3. Die Korrektur im Profil behebt nur das Symptom. Solange die Tracking-Nummer nirgends sonst auftaucht, kommt der Vorschlag wieder.
4. Die Trackingquote im CRM ist **kein** verlässlicher Indikator. Der einzige belastbare Test ist der direkte Abgleich Profilnummer gegen Sollnummer.
5. Monatliche Kontrolle, nicht anlassbezogen.

---

## Der Mechanismus

`evidenz: eigener-test`
Erhebung vom 27.08.2026 über 24 Profile von SEO-Kunden: Bei fünf stand nicht die
hinterlegte Tracking-Nummer im Profil, sondern eine andere. In einem Fall
(Kanalservice CS, Passau) war es nachweislich die echte Festnetznummer des Betriebs,
und die Trackingquote lag bei null — über den gesamten Messzeitraum kein einziger
erfasster Anruf.

Google gleicht Profildaten mit dem ab, was es sonst über den Betrieb findet:
Impressum, Website, Branchenverzeichnisse, Altbestände. Eine Tracking-Nummer steht
per Definition nur an einer Stelle — im Profil. Die echte Nummer steht überall
sonst. Aus Googles Sicht ist das Profil damit der Ausreißer, und die Korrektur
läuft als „Aktualisierung durch Google".

`evidenz: branchenbehauptung` für die Ursachenzuschreibung. Google erklärt nicht,
woraus es Korrekturen ableitet. Das Muster ist aber konsistent.

---

## Warum das teuer ist

Anders als eine Sperrung fällt der Fall nicht auf. Das Profil bleibt sichtbar, es
rankt unverändert, die Bewertungen laufen weiter. Nur die Zuordnung bricht ab.

In der Auswertung sieht es dann so aus, als hätte die Sichtbarkeit nachgelassen —
tatsächlich telefoniert der Kunde weiter, nur an der Messung vorbei. Wer die
Wirkung seiner Arbeit belegen muss, verliert genau dort den Nachweis.

Nebeneffekt: Die Tracking-Nummer wird weiter gemietet. Bei Kanalservice CS
1,80 USD im Monat für eine Nummer ohne einen einzigen Anruf.

---

## Was nicht funktioniert

`evidenz: eigener-test`
Die Vermutung lag nahe, eine niedrige Trackingquote sei ein Frühindikator. Der
Abgleich widerlegt das:

| Kunde | Trackingquote | Nummer im Profil |
|---|---|---|
| Bota-Rohrservice | 32 % | korrekt |
| Technische Rohrreinigung | 52 % | korrekt |
| Scheithauer Mössingen | 45 % | korrekt |
| Haas | 50 % | korrekt |
| Rohrteufel | 51 % | **falsch** |
| Kanalservice CS | 0 % | **falsch** |

Nur der Extremwert null war aussagekräftig. Quoten zwischen 30 und 60 Prozent haben
andere Ursachen — Anrufe über Kanäle ohne Tracking-Nummer, Direktwahl aus dem
Adressbuch, Weiterempfehlungen.

**Konsequenz:** Der Abgleich muss auf der Nummer selbst stattfinden, nicht auf einer
abgeleiteten Kennzahl.

---

## Prüfverfahren

Pro Profil unter einer Minute:

1. Sollnummer aus der Tracking-Plattform holen — die mit Quelle „Google My Business",
   nicht irgendeine aus dem Block. Betriebe haben oft sechs bis dreißig Nummern für
   verschiedene Kanäle.
2. Betriebsnamen plus Ort bei Google suchen und die Nummer im Profil ablesen.
3. Vergleichen. Bei Abweichung: prüfen, ob die gefundene Nummer überhaupt eine
   Tracking-Nummer ist oder die echte Anschlussnummer.

**Fallstrick:** Nummern aus demselben Block unterscheiden sich oft nur in der letzten
Ziffer. `9529980` und `9529984` sehen fast gleich aus und sind zwei verschiedene
Kanäle. Ziffernweise vergleichen.

---

## Vorbeugen statt reparieren

Die Korrektur im Profil hält nur, wenn der Widerspruch verschwindet. Dafür muss die
GMB-Nummer außerhalb des Profils belegbar sein:

1. **Impressum.** Die Tracking-Nummer dort als Kontaktnummer führen oder zusätzlich
   aufnehmen.
2. **Hauptverzeichnisse.** Das Örtliche, Gelbe Seiten, Handwerkskammer- und
   Innungsverzeichnis mit derselben Nummer.
3. **Website konsistent halten.** Der häufigste Fehler: Auf einer Seite steht die
   Tracking-Nummer, auf der nächsten die echte, auf der dritten eine alte aus einem
   früheren Relaunch. Bei Kanalservice CS standen drei verschiedene Nummern
   nebeneinander, darunter eine, die in der Tracking-Plattform als „Alte Website"
   markiert war.

`evidenz: branchenbehauptung` — plausibel und konsistent mit dem beobachteten
Verhalten, aber nicht von Google bestätigt. Ob die Ersetzung danach ausbleibt,
lässt sich erst über mehrere Monate beurteilen. Offener Punkt.

---

## Kontrollroutine

- **Monatlich** alle betreuten Profile abgleichen. Aufwand bei 30 Profilen unter
  einer halben Stunde.
- **Immer nach** einer Adress- oder Namensänderung am Profil.
- **Immer nach** einem Website-Relaunch.
- **Sofort**, wenn eine „Aktualisierung durch Google" im Dashboard auftaucht.

Der Idealzustand ist automatisch: Place-ID je Standort hinterlegen, Profilnummer
per API abfragen, gegen die Sollnummer prüfen, bei Abweichung melden. Voraussetzung
ist eine Place-ID **pro Standort** — wenn sie am Projekt hängt, tragen alle
Standorte eines Mehrstandortkunden dieselbe ID und der Abgleich läuft ins Leere.

---

## Häufige Fehler

- **Nur bei Auffälligkeit prüfen.** Der Fall ist per Definition unauffällig.
- **Auf die Trackingquote verlassen.** Siehe oben, funktioniert nicht.
- **Nummer im Profil korrigieren und Website lassen.** Der Vorschlag kommt wieder.
- **Falsche Nummer aus dem Block gesetzt.** Ohne Kanalzuordnung landet der Anruf in
  der falschen Auswertung.
- **Mehrere Profile am selben Tag ändern.** Erhöht das Prüfrisiko, siehe
  `28-servicegebiet-und-standort.md`.

---

## Abgrenzung

- Adressänderungen und Profilsperrungen → `28-servicegebiet-und-standort.md`
- Umgang mit „Aktualisierungen durch Google" allgemein → `30-sop/36-sop-profil-schutz.md`
- NAP-Konsistenz über Verzeichnisse → `22-name-und-nap.md`

---

## Offene Punkte

| Frage | Wie klären | Priorität |
|---|---|---|
| Bleibt die Ersetzung aus, wenn die Nummer im Impressum steht? | Bei 5 korrigierten Profilen Nummer im Impressum ergänzen, 6 Monate beobachten | hoch |
| Wie oft passiert das im Bestand? | Monatliche Kontrolle protokollieren, Häufigkeit auswerten | hoch |
| Lässt sich der Abgleich über die Places API automatisieren? | Prüfen, sobald Place-ID je Standort vorliegt | mittel |
| Woraus genau zieht Google die Ersatznummer? | Bei einem Fall alle Fundstellen der Ersatznummer im Netz erheben | niedrig |

---

## Quellen

- Eigene Erhebung 27.08.2026, 24 Profile von SEO-Kunden, Abgleich Profilnummer gegen
  hinterlegte GMB-Tracking-Nummer. Fünf Abweichungen, alle korrigiert.
- Google Unternehmensprofil-Hilfe, Aktualisierungen durch Google —
  support.google.com/business
