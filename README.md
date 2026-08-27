# GBP-Playbook

Belegtes Playbook für die Optimierung und Messung von Google-Unternehmensprofilen
im Kanalservice/Rohrreinigung, Markt DACH.

## Prinzip

Vier Arten von Inhalt, strikt getrennt:

| Ebene | Ordner | Frage, die sie beantwortet |
|---|---|---|
| Wissen | `10-grundlagen/`, `20-wissen/` | Was wirkt, und wie gut ist es belegt? |
| Verfahren | `30-sop/` | Was tue ich konkret, in welcher Reihenfolge? |
| Messung | `40-messung/` | Woran sehe ich, ob es gewirkt hat? |
| Belege | `90-quellen/` | Woher stammt die Aussage? |

**Nicht in dieses Repo gehören Kundendaten.** Zustand, Zugänge und Messwerte einzelner
Profile liegen in Notion bzw. Supabase. Hier steht nur, was für alle Kunden gilt.

## Evidenzstufen

Jede Aussage bekommt eine Stufe. Ohne Beleg lieber „unklar" schreiben als plausibel klingen.

| Stufe | Bedeutung |
|---|---|
| `google-doku` | Steht so in Googles offizieller Dokumentation oder Richtlinie. |
| `studie` | Aus einer veröffentlichten, methodisch nachvollziehbaren Erhebung. |
| `branchenquelle` | Aus mehreren unabhängigen Fachquellen, aber nicht von Google bestätigt. |
| `eigener-test` | Von uns selbst gemessen. Testdesign in `40-messung/` verlinken. |
| `branchenbehauptung` | Agenturmeinung, plausibel, unbelegt. Kandidat für einen eigenen Test. |
| `unklar` | Wissen wir nicht. Gehört in „Offene Punkte". |

US-Quellen (YouTube, Newsletter, Agenturblogs) sind Input, keine Wahrheit. Immer gegen
Googles Richtlinien, deutsche Rechtslage (UWG, DSGVO) und den DACH-Markt prüfen.
Taktiken, die dagegen verstoßen, werden klar als solche benannt — auch wenn sie wirken.
Wir betreuen fremde Profile und haften dafür.

## Dateikonvention

Markdown mit YAML-Frontmatter, Vorlage in `50-vorlagen/51-frontmatter-vorlage.md`.
Nummernpräfixe sind stabile Referenzen: eine Datei behält ihre Nummer auch bei Umbenennung.

## Status

`status: geprueft` setzt nur der Owner des Repos. Alles andere bleibt `entwurf`.
Das ist der einzige Mechanismus, der verhindert, dass Ungeprüftes wie belegtes Wissen aussieht.

Aktueller Ausbaustand und nächste Schritte: `00-start-hier.md`
