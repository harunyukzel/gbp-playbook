---
titel: Frontmatter-Vorlage
typ: wissen
evidenz: n/a
verifiziert_am: 2026-08-27
naechste_pruefung: 2027-08-27
gilt_fuer: kanalservice-dach
owner: harun
status: geprueft
---

# Frontmatter-Vorlage

Kopf jeder neuen Datei:

```yaml
---
titel:              # Klartext, nicht der Dateiname
typ:                # wissen | sop | messung
evidenz:            # google-doku | studie | branchenquelle | eigener-test |
                    # branchenbehauptung | gemischt
quelle:             # URL oder Kurzbeleg; bei gemischt: je Aussage im Text
verifiziert_am:     # YYYY-MM-DD
naechste_pruefung:  # YYYY-MM-DD
gilt_fuer:          # kanalservice-dach | kanalservice-de | alle
owner:              # harun | lukas | junior
status:             # entwurf | geprueft | veraltet
---
```

## Aufbau im Text

Jede Wissensdatei enthält:

1. **Kurzfassung** — 3 bis 5 Sätze, die auch allein Sinn ergeben
2. **Hauptteil** — Aussagen einzeln mit `evidenz:` ausgezeichnet, wenn die
   Datei im Frontmatter `gemischt` trägt
3. **Häufige Fehler** — was in der Praxis schiefgeht
4. **Abgrenzung** — was hier *nicht* steht und wo es stattdessen steht
5. **Offene Punkte** — Tabelle: Frage / wie klären / Priorität
6. **Quellen**

Jede SOP-Datei enthält zusätzlich:

- **Voraussetzungen** — was vorher erledigt sein muss
- **Definition of Done** — woran erkennt man, dass der Schritt fertig ist
- **Freigabe nötig** — ja/nein, und von wem

## Prüfrhythmus

`naechste_pruefung` setzen nach Änderungsfrequenz des Themas:
Google-Richtlinien halbjährlich, eigene Testergebnisse jährlich,
Kategorielisten halbjährlich.
