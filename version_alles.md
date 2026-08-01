# NODALYS – Produktspezifikation (Gesamtdokument)

> version_alles — vollständiges Spec-Dokument, unverändert 1:1 aus dem Gründertreffen-Briefing übernommen. Referenzierte, aber im Quelltext nicht ausformulierte Abschnitte (20 Detailtiefe zu Consent-Alternativen, 24 bekannte Prototyp-Abweichungen, 27 offene Punkte) werden hier als Verweis belassen, nicht erfunden.

## 1. Produktkern [Beide]

- Name: NODALYS. Kategorie: ADHS-Tracking- und Lifestyle-App, ausdrücklich kein Medizinprodukt und keine medizinische App.
- Architektur: Local-First, Privacy-by-Design. Keine Pflicht-Cloud, kein Account-Zwang, kein Server für Gesundheitsdaten, keine Datenweitergabe, keine Werbung.
- Plattform: Smartphone-first, iOS + Android parallel, automatisches iPad-Layout. Sprachen: Deutsch + Englisch von Launch an, Umschalter jederzeit sichtbar (siehe Abschnitt 5).
- Grundidee: Menschen mit ADHS (oder Verdacht) erfassen persönliche Faktoren (Fokus, Stimmung, Energie, Schlaf, Stress, Ernährung, Zyklus, Medikation u. a.) und sehen sie über Zeit visualisiert – ohne Diagnose, Bewertung oder Interpretation.
- **Kernprinzip „keine Interpretation":** Die App erkennt keine Ursachen, gibt keine Empfehlungen, bewertet keine Lebensweise. Erlaubt: Diagramme, Zeitverläufe, Wertevergleiche, zeitliche Marker (z. B. Medikamentenwechsel). Nicht erlaubt: Aussagen wie „Wenig Schlaf verursacht deine Fokusprobleme" oder jede andere Korrelations-Sprache.
- Keine Schuldmechanismen: kein „Du hast X Tage nichts eingetragen", keine Strikes, keine Streaks.
- View-Tree-Entfernung: nicht aktivierte Module verschwinden vollständig aus Menü, Widgets und Erinnerungen – nicht nur aus der Ansicht.
- Design-Grundregeln: wenige Schritte, ruhige/klare Oberfläche, One-Touch-Eingaben wo möglich, wenig visuelle Reize.
- Permanenter, dezenter Disclaimer „kein Medizinprodukt" ist auf der Begrüßung und im Hauptbereich „Heute" dauerhaft sichtbar.

## 2. Zielgruppe & Positionierung [Beide]

- Primär: Menschen mit ADHS oder ADHS-Verdacht, auch ohne bestätigte Diagnose nutzbar. Besonderer Fokus auf Frauen mit ADHS. Eigener Kinderbereich zusätzlich (Abschnitt 11).
- Altersgruppe Erwachsenenversion grob 4–45 Jahre, alle Geschlechter, Einkommen nicht begrenzt. Gesuchte Werte: Vertrauen, Innovation, Professionalität.
- Positionierungs-Tendenzen: eher modern als traditionell, eher minimalistisch als verspielt, mittig klassisch/trendy, eher sympathisch/warm als konservativ, eher zugänglich/günstig als premium/exklusiv, mittig maschinell/organisch, mittig viel Information/reduziert.

## 3. Wettbewerbsanalyse [Beide]

Ehrliche Einordnung, nicht nur Eigenwerbung – Recherche nicht erschöpfend, vor Pitch/Förderantrag vertiefen. Wird bei größeren Produktänderungen aktualisiert.

### Erwachsenenbereich

| App | Stärken | Wo NODALYS vorne liegt | Wo der Wettbewerber stärker ist |
|---|---|---|---|
| Bearable | ~900.000 Nutzer, eingespielt, zeigt aktiv Korrelationen zwischen Medikation/Symptomen, breite Faktoren-Auswahl | Local-First (Bearable ist cloud-basiert), kein Korrelations-Framing sondern neutrale Visualisierung, Deutsch von Anfang an | Reifegrad/Nutzerbasis, mehr Jahre Produktentwicklung, vermutlich mehr vorgefertigte Insight-Vorlagen |
| Clue | Marktführer Zyklus-Tracking, sehr detailliertes Symptom-Set (200+), etabliertes Vertrauen im Zyklusbereich | ADHS-Bezug fehlt bei Clue komplett, kein Local-First | Reine Zyklus-Tiefe/-Genauigkeit vermutlich höher als NODALYS' bewusst prognosefreies Zyklusmodul |
| Dhara, Nuro, CareClinic | Medikations-/Symptom-Korrelation, teils HIPAA-konform | Local-First, Deutsch, kein Korrelations-Framing | Nicht im Detail recherchiert – keine belastbare Aussage möglich |

### Kinderbereich (neu recherchiert, weil Teil des Produkts)

- Bearable hat Kinderprofile nur als offenen Feature-Wunsch auf der Roadmap, nicht verfügbar. Echter, aktueller Vorsprung für NODALYS, sofern der Kinderbereich tatsächlich ausgeliefert wird.
- Clue schließt Nutzer:innen unter 13 komplett aus (COPPA-Selbstauskunft beim Setup), keine eigene Kindererfahrung. Clue hat zudem eine „mit Freunden teilen"-Funktion, die von Dritten (Mozilla Foundation, SaferKid) als Mobbing-/Fremdkontakt-Risiko eingestuft wird – ein konkreter Grund, warum NODALYS keine Social-Sharing-Funktion im Kinderbereich haben sollte.
- Dedizierte Kinder-ADHS-Apps existieren bereits (Joon, Goally, Understood, Brili u. a.), allerdings mit anderem Fokus: Verhalten, Routinen, Aufgaben, mit Eltern-Dashboard. Keine kombiniert das mit Medikations- oder Zyklus-Tracking. Angrenzender, nicht identischer Wettbewerb.
- Ehrliches Fazit: Die tatsächliche Lücke ist nicht „irgendeine App für Kinder mit ADHS", sondern die Kombination aus Eltern-Proxy→Self-Report-Übergang, Medikations-/Zyklus-Tracking und Local-First bei Minderjährigen. Im Pitch präzise formulieren, nicht als „es gibt nichts Vergleichbares".

## 4. Design-System [Beide]

Grundschrift: Serif (Georgia) für Überschriften, System-Sans für Fließtext/UI. Radius-System: `--radius` (20px) für Karten, `--radius-sm` (12px) für kleinere Elemente. Im Kids-Mode größer: 28px/18px.

**Farben Erwachsenenversion – Light:** Sand #EAE1CE / #F4EDDD / #DED2B7, Ink #332E27 / #7A7263 / #A69E8C, Blau #54628F / #DCE1EE, Rose #C0808A / #F1DEE0, Grün #6E8F6E / #DEE7DA, Lila #8B7FBF / #E4DFF3.

**Farben Erwachsenenversion – Dark** (via `body.dark`): Sand-Töne auf #221F1B / #2B2721 / #3A352C, Ink auf #EDE6D8 / #B5AC9A / #847C6C, übrige „soft"-Farben entsprechend abgedunkelt.

**Farbwelt Kinder-Interface** (eigenständiges Farbschema, nicht identisch mit der Erwachsenenversion):

```
--sand:#EAE1CE; --sand-card:#F4EDDD; --sand-border:#DED2B7;
--ink:#332E27; --ink-soft:#7A7263; --ink-faint:#A69E8C;
--blue:#4A9BB0; --blue-soft:#DCEFF0;
--red:#BC6B5A; --red-soft:#F0DCD3;
--green:#6E8F6E; --green-soft:#DEE7DA;
--purple:#8B7FBF; --purple-soft:#E4DFF3;
--gold:#D8A657; --gold-soft:#F1E3C7;
```

Formensprache Modul-Icons (Kinder wie Erwachsene): dick umrandet, organisch, keine Gesichter, gedeckte Flächenfarbe mit „soft"-Hintergrundton.

## 5. App-Gerüst / Navigation [Beide]

- Smartphone-Mockup (400px breit, abgerundeter Rahmen, Statusleiste), lokal im Browser lauffähig.
- Zurück-Button oben links, sichtbar außerhalb Welcome/Haupt-Tabs, mit Navigationshistorie (navHistory) – Zurückgehen im Onboarding ist damit an jeder Stelle möglich und ist eine feste Anforderung, kein optionales Detail.
- Sprachumschalter DE/EN oben rechts, bereits auf dem allerersten Bildschirm (Begrüßung/Welcome) sichtbar und wirksam – nicht erst nach dem Onboarding zuschaltbar. Wirkt sofort auf alle sichtbaren Texte (data-i18n-Attribute + zentrales DICT-Objekt).
- Light/Dark-Mode umschaltbar.
- Bottom-Nav mit drei Tabs, erscheint erst nach Abschluss des Onboardings:
  - Erwachsenenversion: Heute / Insights / Einstellungen.
  - Kinderversion: Heute / Einblicke / Einstellungen – „Einblicke" ersetzt bewusst die ursprüngliche Bezeichnung „Meine Muster", da „Muster" bereits eine Bewertung suggeriert und damit im Spannungsfeld zum Nicht-Interpretations-Prinzip (Abschnitt 1) steht. „Einblicke" (EN: „Insights") klingt eher nach Ansicht/Zugang als nach Bewertung. Inhalt bleibt rein visuell (Diagramme, Zeitverläufe, keine bewertenden Texte).
- Modal-System für alle Detail-Ansichten (Settings-Unterseiten, Paywall, FAQ, Tages-Rückblick).
- Toast-Benachrichtigung mitte (z. B. „Gespeichert ✓" im Prototyp) bei jeder Dateneingabe.
- Keine Emojis – gilt für beide Versionen, ausnahmslos. Das betrifft auch Statusleisten-Symbole, Modul-Icons, Speichern-/Löschen-Zeichen, Warnhinweise, Avatar-Platzhalter usw. Die Kinderversion wird stattdessen mit eigens gestalteten, markenkonformen Illustrationen/Icons ansprechend gestaltet (Abschnitt 6). Der aktuelle Prototyp-Code verwendet an vielen Stellen noch Unicode-Emojis; das ist eine bekannte, zu behebende Abweichung (Abschnitt 24).

## 6. Icon-System [Beide]

Gezielte Änderungen/Ergänzungen gegenüber dem bisherigen Icon-Entwurf, Rest unverändert:

| Icon | Stand |
|---|---|
| Essen | ersetzen durch Teller + Messer + Gabel (konkret gegenständlich statt abstrakt) |
| Süßigkeiten | neu, eigenes Icon getrennt von „Essen": Lolli + Eis |
| Stimmung | ein generisches Herz-/Blob-Icon (Rose, wird zu Rot); ab 9 Jahren ersetzen durch Symbol mit mehreren Gefühlen (z. B. Reihe kleiner Ausdrucks-Icons statt einem generischen Icon); für unter 9 Jahren kann das einfache Icon bleiben |
| Periode | Tropfen-Form (Rose, wird zu Rot) |
| Einstellungen | ersetzen durch Werkzeug-/Schraubenschlüssel-Symbol |
| Schule (Kinder) | neu, eigenes Modul-Icon |
| Arbeit/Uni (Erwachsene, ab 17/18 Jahre) | existiert nicht → neu, eigenes Modul-Icon |

Formensprache (dick umrandet, organisch, keine Gesichter, gedeckte Flächenfarbe mit „soft"-Hintergrund) bleibt für alle neuen/geänderten Icons erhalten.

## 7. Onboarding [Beide]

Schritt für Schritt, inkl. Zurück-Navigation an jeder Stelle (Abschnitt 5):

1. **Begrüßung:** Claim „100% Lokal & Privat", Markenname, Kurzerklärung, permanenter Disclaimer „kein Medizinprodukt", Sprachumschalter DE/EN bereits hier aktiv, Start-Button. Inhalte mittig angeordnet.
2. **Name:** Freitextfeld.
3. **Profil:** Geschlechter-Auswahl (Weiblich/Männlich/Divers/Keine Angabe – biologisches Geschlecht getrennt von Geschlechtsidentität) + optionale Felder Größe, Gewicht.
   - Alter ausschließlich über Geburtsdatum (kein freies Zahlenfeld) oder ganz weglassbar. Der automatische Stufenwechsel im Kinderbereich (Abschnitt 11) braucht ein echtes Geburtsdatum. Wer das Geburtsdatum weglässt, muss aktiv „Ich bin mindestens 16 Jahre alt" bestätigen (Pflicht-Checkbox; genauer Wortlaut noch offen, Abschnitt 27). Bei angegebenem Erwachsenen-Geburtsdatum zusätzlich eine Wahrheitsbestätigung („ich bestätige, dass diese Angabe stimmt") vorsehen – im aktuellen Prototyp noch nicht umgesetzt (Abschnitt 27).
   - Ist das berechnete Alter unter 16 Jahre → Kids-Modus aktivieren, Altersstufe intern gemäß dem harmonisierten Modell (Abschnitt 11) speichern, weiter zu Eltern-Einwilligung.
   - Sonst direkt weiter zur Fokus-Auswahl.
4. **Eltern-Einwilligung (nur wenn Alter < 16):** Name der erziehungsberechtigten Person, Pflicht-Checkbox „Ich bin erziehungsberechtigt und willige ein …" (Bestätigen-Button bleibt deaktiviert bis angehakt), Verweis auf Art. 8 DSGVO im Text, Prototyp-Hinweis, dass dies nur eine Selbstauskunft ohne Identitätsprüfung ist. Kindgerechtes Design ganz unten in der Stufenlogik verankert. Rechtlich reicht eine reine Checkbox-Selbstauskunft vermutlich nicht als „verifiable consent" – siehe Abschnitt 20 zu den geprüften Alternativen.
5. **Fokus-Bereiche:** Mehrfachauswahl-Pills aus Fokus, Stimmung, Energie, Schlaf, Stress, Medikation, Zyklus, Hormone, Ernährung, Libido (die beiden letzteren ergänzen die ursprüngliche Liste, siehe Abschnitt 8). Zyklus wird herausgefiltert bei biologischem Geschlecht „männlich" oder bei der jüngsten Kinder-Altersstufe.
6. **Nutzungsgrund:** Einfachauswahl „Ich habe ADHS" / „Ich vermute ADHS" / „Ich befinde mich in Abklärung" / „Ich möchte meine Muster allgemein verstehen".
7. **Medikamentenfrage:** Entschieden, an den Nutzungsgrund gekoppelt (alte, maßgebliche Logik): Bei Nutzungsgrund „Ich habe ADHS" wird gezielt „Nutzt du ADHS-Medikamente?" gefragt, bei den übrigen Gründen allgemein „Nimmst du Medikamente?".
8. **Medikament hinzufügen** (nur wenn Ja/Manchmal – bei „Nein" oder „Keine Angabe" wird dieser Schritt vollständig übersprungen, es wird nicht nach konkreten Medikamenten gefragt): Freitext Wirkstoff/optionale Dosis, Häufigkeit (1–openend täglich, Dropdown), „+ Weiteres Medikament speichern" fügt der Liste hinzu, „Weiter" und „Später in den Einstellungen" committen beide die bisherige Liste. In den Einstellungen bleibt der Menüpunkt „Medikamente/Wirkstoff" unabhängig davon immer sichtbar, falls später doch Medikamente ergänzt werden sollen.
9. **Zyklus-Frage** (nur wenn Geschlecht ≠ männlich und nicht jüngste Kids-Stufe): Ja/Nein/Später + auffälliger Hinweis-Banner „NODALYS dient nicht der Verhütung".
10. **Hormoneller Status** (nur wenn Zyklus = Ja und nicht Kids-Modus): Verhütung / Schwangerschaft / Perimenopause / Keiner.
11. **Allgemeines Hormone-Modul:** Ja/Nein/Später, Beispieltext passt sich an (Kids: nur Pubertät; männlich: Pubertät/Testosteron; sonst: Pubertät/Wechseljahre). Für die jüngste Kinder-Altersstufe (Eltern-Proxy, ca. 4–8 Jahre) passt inhaltlich weder die Zyklus- noch die allgemeine Hormone-Frage (Pubertät/Wechseljahre sind da nicht relevant) – für diese Stufe beide Fragen im Onboarding auslassen, Modul später über die Einstellungen aktivierbar. Noch nicht final bestätigt.
12. **Health-Sync:**
    - Erwachsenenversion: Apple Health / Google Health Connect verbinden oder überspringen, bleibt Teil des Onboardings.
    - Kinderversion: Health-Import ist nicht Teil des Pflicht-Onboardings, sondern ein granularer Opt-in später in den Einstellungen, zusätzlich abgesichert über die Eltern-PIN (Abschnitt 11). Der aktuelle Prototyp führt diesen Schritt noch für alle Nutzer:innen gleich durch – bekannte Abweichung (Abschnitt 24).
    - Für beide Versionen: die Regel „nur ein Profil pro Gerät darf Health-Daten importieren" (Abschnitt 15) muss bereits im Onboarding sichtbar sein, über ein antippbares Info-Icon, das kurz erklärt, warum das technisch so ist.
13. **Erinnerungen:** Medikamenten-Erinnerung (genommen ja/nein) + Abend-Recap, beide als Toggle, rein optional. Wird die Medikamenten-Erinnerung mit „genommen" bestätigt, erzeugt das automatisch einen Eintrag im Tages-Log/Verlauf (nicht nur eine Benachrichtigung ohne Spuren). **Ganz wichtig.**
14. **Tracking anpassen:** Bis zu drei Module kostenlos wählbar (Basis-Version), weitere Module zeigen ein „PRO"-Badge und öffnen bei Auswahlversuch die Paywall. Muss jederzeit in den Einstellungen änderbar sein, nicht nur einmalig im Onboarding festlegbar. Bei Kindern kann die App nur mit Erlaubnis der Eltern über eine PIN im App Store gekauft werden.
15. **Fertig-Screen:** Zusammenfassung der aktiven Module, „App öffnen" startet die Hauptnutzung, kein erneutes Onboarding bei täglicher Nutzung danach.

## 8. Modul-System [Beide]

Nutzer:innen aktivieren Module selbst: Fokus, Stimmung, Energie, Schlaf, Stress, Ernährung, Bewegung, Zyklus/Hormone, Medikation, Libido, individuelle Faktoren. Nicht aktivierte Module verschwinden vollständig aus der App (View-Tree-Entfernung, Abschnitt 1).

Neue Module aus dem Kinder-Interface-Prompt, zusätzlich zur obigen Liste:
- Schule (Kinder-Interface): eigenes Modul, gleichrangig zu Konzentration/Stimmung/Energie/Schlaf, mit eigenem Dashboard-Bereich, kein einzelner Faktor.
- Arbeit/Uni (Erwachsenen-Interface): analog eigenes Modul, ergänzend zum bereits bestehenden Faktor „Arbeitsbelastung".

Libido-Modul: primär als Quick-Track/Smart-Tag-Kategorie umgesetzt (siehe Abschnitt 9), nicht als tiefes Detail-Modul – Funktionsumfang damit geklärt.

Support: maximal eine E-Mail-Adresse zum Launch, keine eigene Hotline. Eine Hotline kommt frühestens infrage, wenn die App so groß ist, dass E-Mail-Support nicht mehr ausreicht.

## 9. Tracking-Eingabe / UI-Elemente [Beide]

Antippbare Zahlen-Kacheln. Jede Skala braucht sichtbare Text-Anker an beiden Enden (z. B. „1 · wenig Stress" / „5 · viel Stress"). Der aktuelle Prototyp-Code nutzt für Fokus/Stimmung/Energie/Stress noch `<input type="range">`-Regler mit Live-Wertanzeige und Speichern beim Loslassen – bekannte Abweichung (Abschnitt 24).

- One-Touch-Prinzip: Einträge möglichst in einem Schritt erfassbar, Speichern löst Toast-Bestätigung + kurzen „gerade gespeichert"-Puls-Effekt aus.
- Schlaf-Karte: Stunden per Stepper (±0,5), zusätzlich 4-stufige Schlafqualität (schlecht/ok/gut/super). Muss aber dann auch auf dem Graphen sichtbar sein.
- Quick Track: horizontal scrollbare, thematische Kategorien zum schnellen Antippen: Stimmung, Kognitiv, Körperlich, Nebenwirkungen (wenn Medikation aktiv), Zyklus (wenn Modul aktiv), Substanzen (nicht im Kids-Modus), Alltag, sowie ergänzend Ernährung (rein qualitativ, z. B. „ausgewogen gegessen", „nur Süßigkeiten", „kein Hunger", „viel gegessen" – keine Kalorien) und Libido als jeweils eigene Kategorien. „+ Eigener Tag" erlaubt freien Text. Ernährung bleibt damit doppelt trackbar: schnell per Quick-Track-Chip und ausführlicher im eigenen Modul.
- Jeder Quick-Track-Eintrag landet sichtbar im Tages-Log und ist danach im Verlauf (Abschnitt 14) nachvollziehbar – die gespeicherte Auswahl bleibt als angetippter/hervorgehobener Chip erkennbar, nicht nur kurz als Toast.
- Einträge müssen auch nachgetragen werden können, z. B. am Dienstag die Einträge von letzter Woche Mittwoch nachtragen.

## 10. Medikamenten-Modul [Beide]

- Erfassung: Wirkstoff (kuratierte Liste + Freitext), Dosis, Zeitpunkt, persönliche Beobachtungen. Mehrere Medikamente gleichzeitig möglich.
- Keine Bewertung der Wirksamkeit, keine Dosierungsempfehlung. Anpassungen jederzeit in den Einstellungen möglich, müssen im Graphen gekennzeichnet werden.
- Dosis-/Medikamentenwechsel werden als vertikale gestrichelte Linie mit Beschriftung im Insights-Diagramm markiert – rein zeitlich, keine Kausalaussage (Abschnitt 1, 13).
- Bei Häufigkeit 1×/Tag: einfacher Kreis-Check-Button auf „Heute". Bei mehrfacher Einnahme: Zähler „X/Y heute genommen" mit Plus/Minus.
- Medikamenten-Erinnerung mit Bestätigung „genommen" erzeugt automatisch einen Tages-Log-Eintrag (Abschnitt 7, Schritt 13).
- Ist auf die Frage „Nimmst du Medikamente?" mit „Nein" oder „Keine Angabe" geantwortet worden, entfällt der nachfolgende Onboarding-Schritt „Medikament hinzufügen" vollständig – es wird nicht nach konkreten Medikamenten gefragt, wenn keine genommen werden. Der Menüpunkt „Medikamente" in den Einstellungen bleibt davon unberührt weiterhin sichtbar, für den Fall einer späteren Ergänzung.

## 11. Zyklus/Hormone-Modul [Beide]

- Erfassung: Periode, Symptome, persönliche Zyklusdaten, hormonelle Verhütung (inkl. Spirale).
- Explizit keine Vorhersage/Prognose – der Zyklus kann sich unter ADHS-Medikation verschieben.
- Perimenopause/Menopause als Option wählbar, ohne im Onboarding redundant nochmal gefragt zu werden.
- Verhütungs-Disclaimer als aktiv anklickbarer „Verstanden"-Button, nicht nur Text – „NODALYS dient nicht der Verhütung".
- Auf „Heute": statischer Demo-Zyklustag, „Zyklus loggen"-Link, zusätzlicher Hinweis, falls hormoneller Status „Verhütung" ist.
- Zyklus-Disclaimer-Banner taucht in Insights erneut auf, sobald der Zyklus-Datenpunkt im aktuellen View enthalten ist.
- Kinderversion: Zyklus-Modul bei Kindern nicht standardmäßig aktiv, sondern in den Einstellungen zu finden – für Nutzerinnen, die ihre Periode noch nicht haben. Ab 9 Jahren muss spätestens die Möglichkeit bestehen, eine bereits eingesetzte Periode einzutragen (relevant, weil sich das auf Medikamentenwirkung/-dosierung auswirken kann).
  - Popup-Trigger: bei Profilen mit biologischem Geschlecht „weiblich" erscheint monatlich ein beiläufig formuliertes Popup mit der Frage, ob die aktuellen Einstellungen noch passen („Hast du deine Periode schon bekommen? Möchtest du das Zyklus-Modul aktivieren?"). Kritischer Hinweis: ein monatliches Intervall steht in gewissem Spannungsfeld zum Prinzip „keine Druckmechanismen" (Abschnitt 1) bei einem sensiblen Thema – bewusst trotzdem so vorgesehen, Formulierung entsprechend beiläufig/undramatisch halten.
  - Verpflichtende Eltern-Einwilligung: Aktivierung des Zyklus-Moduls bei Minderjährigen erfordert einen Consent-Screen, bestätigt per Eltern-PIN (Abschnitt 12). Rechtlich relevant: COPPA (<13 USA) / DSGVO-K (<16 DE) – Gesamtprüfung noch offen (Abschnitt 20, 27).

## 12. Profile, mehrere Nutzer:innen & Kinderbereich [Beide]

**Mehrere Profile pro Gerät:**
- Normalfall: jede Person hat ihre eigene Installation auf ihrem eigenen Gerät, völlig getrennt.
- Nischenfall (geteiltes Gerät): lokaler Profil-Umschalter mit PIN/FaceID pro Profil, alle Profile in derselben lokalen Datenbank, kein Server-Sync.
- Logout-Button, um das aktuelle lokale Profil zu verlassen (relevant v. a. beim Profilumschalter auf einem gemeinsam genutzten Gerät) – kein Datenlöschen, nur Wechsel/Abmelden.
- Profil muss nachträglich bearbeitbar sein (Name, Gewicht, Größe, Geburtsdatum etc.).

**Kinderbereich – harmonisiertes Altersstufen-Modell:**

| Stufe | Verhalten |
|---|---|
| Ab 4 Jahren | App nutzbar, Eltern-Proxy-Tracking beginnt: Eltern tragen stellvertretend ein. Kinder-Interface mit einfachem Stimmungssymbol. Premium-Käufe erfordern die Eltern-PIN. |
| Ab 5–6 Jahre | Kinder können zusätzlich selbst eintragen, Proxy-Tracking bleibt parallel möglich. Kein fest codiertes Umschalt-Alter: Eltern entscheiden individuell pro Profil über ein Eltern-Setting „Proxy-Tracking aktiv" (an/aus). Premium-Käufe erfordern die Eltern-PIN. |
| 9–12 Jahre | Erweitertes Stimmungssymbol mit mehreren Gefühlen, Self-Report wird zum Standard. Spätestens ab 9 Jahren: Möglichkeit, eine bereits eingesetzte Periode einzutragen. Premium-Käufe erfordern die Eltern-PIN. |
| Ab 13 Jahre | Automatischer Wechsel ins Erwachsenen-Interface (UI-Ebene). Avatar wechselt standardmäßig zu „Halbton-Split" (Wahlmöglichkeit, die Tier-Silhouette aus der Kinderstufe stattdessen zu behalten). Premium-Käufe erfordern die Eltern-PIN. |
| Bis 16 Jahre (unabhängig von der UI-Stufe) | Eltern-Consent-Gültigkeit bleibt bestehen: Premium-Käufe, Aktivierung des Zyklus-Moduls und Aktivierung des Health-App-Imports erfordern weiterhin die Eltern-PIN (Abschnitt 12) – auch bei 13–15-Jährigen, die bereits im Erwachsenen-Interface sind. |

Proxy-Tracking-Mechanik: Eltern-Proxy-Einträge werden ins Kind-Profil eingebettet, jeder Eintrag auf Eintragsebene (nicht Profilebene) mit „von Elternteil eingetragen" markiert. Das Profil wandert später selbst in Self-Report- und dann Erwachsenen-Modus, die Historie bleibt erhalten.

**Consent & Recht (Kinder), noch nicht final:**
- Einheitliche, strengere Grenze von 16 Jahren für die Eltern-Consent-Pflicht, unabhängig vom Markt (bewusste Übererfüllung des COPPA-Minimums von 13).
- Davon getrennt: die UI-Wechsel-Grenze (13 Jahre) – das Interface kann ab 13 „erwachsen" wirken, während die Eltern-Consent-Gültigkeit im Hintergrund bis 16 bestehen bleibt.
- Reine E-Mail-Bestätigung reicht vermutlich nicht als „verifiable consent". Realistische Optionen: E-Mail + Sicherheitsfragen, Text-Plus (SMS + Zusatzschritt, nur erlaubt weil NODALYS keine Daten an Dritte weitergibt), ID-Verifizierungsdienst (Vouched/Mitek/Jumio, ca. 1–3 $/Prüfung), signiertes Formular, Kreditkarten-Verifizierung, Video-Bestätigung.
- Allgemeine DSGVO-Baustelle: Einwilligungs-Flow, Datenexport, Löschfunktion, Verschlüsselung – juristische Prüfung zwingend vor Umsetzung.
- Aktueller Prototyp: Consent-Screen für unter 16 existiert (Name der erziehungsberechtigten Person + Checkbox), ausdrücklich als reine Selbstauskunft ohne Identitätsprüfung gekennzeichnet.
- Eigenes NODALYS-Eltern-PIN (kein Rückgriff auf native Store-Kindersicherung wie Apple „Ask to Buy" oder Google Family Link), wird verwendet für: Premium-Käufe/-Upgrades bei Nutzer:innen < 16 Jahre, Aktivierung des Zyklus-Moduls, Aktivierung des Health-App-Imports. Genauer Onboarding-Flow für die PIN-Vergabe durch ein Elternteil noch zu spezifizieren (Abschnitt 27).
- Rechtlich relevant: COPPA (<13 USA), DSGVO-K/Art. 8 DSGVO (<16 DE) – Gesamtprüfung laut TODO-Dokument noch offen.

> Hinweis: die gesamte Kinder-Consent-Logik in diesem Dokument ist als Entwurf/Diskussionsstufe fürs Gründertreffen zu behandeln, nicht als rechtlich geprüfte Lösung – nichts davon geht in absehbarer Zeit live.

**Avatar-System – drei Altersstufen:**
- Unter 13 Jahre: vereinfachte Tier-Silhouetten. Keine Fotos bei Kinderprofilen, nur Silhouette (Farbe + Form, kleine kuratierte Auswahl).
- 13–15 Jahre: Standard ist „Halbton-Split" (Kreis, zweigeteilt in zwei Flächentöne derselben Farbfamilie). Zusätzlich optional: die Tier-Silhouette aus der Kinderstufe beibehalten statt zu wechseln – kein Zwangswechsel, frei wählbar im Einstellungsmenü.
- Ab 16 / Erwachsenenversion: zwei Optionen zur Auswahl („Reine Farbfläche" entfällt): Initiale in Serif (Kreis mit einem Buchstaben in Georgia) oder ein sehr zurückhaltendes, dünnes Linien-Icon ohne Fläche.
- Farbgebung aller Avatar-Stufen folgt Abschnitt 4 (Rose → Rot im Kinderbereich, restliche Palette unverändert).

## 13. Hauptbereich „Heute" [Beide]

- Zeitabhängige Begrüßung (Morgen/Tag/Abend) + Name.
- Medikamenten-Karte(n) wie in Abschnitt 10 beschrieben.
- Zyklus-Karte (falls aktiv) und Hormone-Karte (falls aktiv) wie in Abschnitt 11 beschrieben.
- Fokus/Stimmung/Energie/Stress: Erfassung über antippbare Zahlen-Kacheln mit Text-Ankern an beiden Enden (Abschnitt 9), Speichern mit Toast-Bestätigung und kurzem Puls-Effekt.
- Schlaf-Karte: Stunden-Stepper (±0,5) + 4-stufige Qualität.
- Quick-Track-Leiste wie in Abschnitt 9 beschrieben, inkl. Ernährung und Libido.
- Permanenter Disclaimer „kein Medizinprodukt" unten.
- Oben linke Ecke DE/EN Schalter.

## 14. Hauptbereich „Insights" / „Einblicke" [Beide]

- Umschalter Einzeln / Kombiniert.
- Oben linke Ecke DE/EN Schalter.
- Zeitraum-Umschalter 7 Tage / Monat / 3 Monate.
- Bei „Einzeln": Tab-Leiste pro aktivem Modul. Bei „Kombiniert": Mehrfachauswahl-Leiste (mind. 1 Modul muss gewählt bleiben).
- Diagramm vs. Tabelle umschaltbar.
- Liniendiagramm selbst gezeichnet (inline SVG), mit sichtbarer Zeitachse (X-Achse) bei jeder Graphenansicht: pro Modul eigene Farbe und eigenes Strichmuster und eigene Punktform (Kreis/Quadrat/Dreieck/Raute) – bewusst nicht nur farbcodiert, aus Rücksicht auf Farbfehlsichtigkeit. Bei „Kombiniert" wird jede Kurve unabhängig normalisiert (Min-Max-Skalierung) und überlagert.
- Medikamenten-/Dosiswechsel als vertikale gestrichelte Linie mit Beschriftung im Diagramm markiert (rein zeitlich, keine Kausalaussage).
- Zyklus-Disclaimer-Banner erscheint erneut, sobald der Zyklus-Datenpunkt im aktuellen Insights-View enthalten ist.
- Legende mit Farbe + Modulname.
- „Verpasste Tage nachtragen" öffnet eine Liste der letzten 5 Tage zum Nacherfassen.
- PDF-Bericht / CSV-Export als Buttons, beide hinter Premium (öffnen die Paywall, wenn nicht Premium; zeigen sonst PRO- bzw. Haken-Badge). Details siehe Abschnitt 17.
- „Verlauf anzeigen": Woche/Monat-Umschalter. Woche zeigt 7 Tageskreise mit Werten des primären aktiven Moduls. Monat zeigt einen echten Kalender-Grid (korrekter Wochentag-Versatz, Tage-im-Monat-Berechnung, Punkt-Markierung an Tagen mit Eintrag, heutiger Tag hervorgehoben, Tippen auf einen Tag öffnet ein Detail-Modal). Monatsnavigation ist zeitlich unbegrenzt. „Zu heute springen"-Link erscheint, sobald man nicht im aktuellen Monat ist.
- Jeder Quick-Track-Eintrag von „Heute" ist im Verlauf sichtbar nachvollziehbar (Abschnitt 9).
- Der heutige, tatsächlich eingegebene Wert von „Heute" fließt live in die sonst synthetisch generierten Demo-Verlaufsdaten ein (letzter Datenpunkt wird überschrieben), damit eigene Eingaben sichtbar werden.

## 15. Health-App-Integration [Beide]

- Einseitiger Datenfluss: Health-App → NODALYS, nie umgekehrt. Jede Kategorie einzeln freigebbar, jederzeit widerrufbar, keine automatische Übernahme, lokale Verarbeitung.
- Pro Gerät darf nur ein Profil Health-Daten importieren (HealthKit/Health Connect sind geräteweit, nicht profilweit organisiert). Muss im Onboarding über ein Info-Icon erklärt werden (Abschnitt 7).
- Erwachsenenversion: Teil des regulären Onboardings.
- Kinderversion: kein Teil des Pflicht-Onboardings, granularer Opt-in später in den Einstellungen mit gut sichtbarem Hinweis, zusätzlich über Eltern-PIN abgesichert (Abschnitt 12).

## 16. Hauptbereich „Einstellungen" [Beide]

Kopfzeile: Avatar-Platzhalter (kein Foto bei Kinderprofilen, siehe Abschnitt 12), Name, Link „Premium freischalten" (ausgeblendet, wenn bereits Premium). Auch bei Erwachsenen kein Foto, immer Avatare.

Zeilen (jede öffnet ein Modal):
- **Nutzerprofil:** Name/Geschlecht/Geburtsdatum/Größe/Gewicht/Status; bei Kids-Modus zusätzlich Altersstufe, Name der einwilligenden Person, Einwilligungsstatus mit „Einwilligung widerrufen"-Button (mit Sicherheitsabfrage) und erneutem Prototyp-Hinweis; Link zur Premium-Verwaltung.
- **Medikamente:** Liste mit Entfernen-Button. Hinzufügen aktuell über Browser-`prompt()`-Dialoge – klar als Prototyp-Notlösung zu behandeln, kein finales UI. Menüpunkt bleibt immer sichtbar, unabhängig davon, ob im Onboarding „keine Medikamente" angegeben wurde (Abschnitt 10).
- **Tracking-Module:** aktive Anzahl vs. Freigrenze (3 im Basis-Tarif), pro Modul ein Schalter, gesperrte Module zeigen PRO-Badge und öffnen bei Aktivierungsversuch die Paywall.
- **Daten & Datenschutz:** Warnhinweis „nur auf diesem Gerät", FaceID/Fingerabdruck-Schalter, Verschlüsseltes-Backup-Schalter, Export-Button (Premium-gated), Löschen-Button (mit Sicherheitsabfrage), sichtbarer „Von Backup wiederherstellen"-Flow (Abschnitt 18).
- **Sprache & Darstellung:** Dark-Mode-Schalter, Sprachanzeige (Verweis auf den Umschalter oben rechts, der bereits ab dem Welcome-Screen aktiv ist).
- **Benachrichtigungen:** Medikamenten-Erinnerung (inkl. automatischem Tages-Log-Eintrag bei Bestätigung) + Abend-Recap, gleiche Schalter wie im Onboarding.
- **Kontakt & Q&A:** Kontakt-E-Mail-Adresse, aufklappbares FAQ mit mindestens 5 Fragen (Medizinprodukt-Klarstellung, Datenspeicherort, Geräte-Umzug via Backup, „erkennt die App ADHS?", Zyklus-Tracker ist keine Verhütung etc.).
- **Hilfe/Notfall:**
  - Erwachsenenversion: 112, TelefonSeelsorge 0800 111 0 111 / 116 123.
  - Kinderversion: Nummer gegen Kummer 116 111.
  - Eltern: Elterntelefon 0800 111 0 550.
  - Hinweis auf lokale Nummern außerhalb Deutschlands.
- **Premium (nur Erwachsenenversion):** Feature-Liste, Aktiv/PRO-Badge, Resttage bei laufendem Trial, Demo-Schalter zum Umschalten, Hinweis, dass echter Kauf nur über App-/Play-Store läuft. Bei Nutzer:innen < 16 Jahre: Premium-Käufe erfordern zusätzlich die Eltern-PIN (Abschnitt 12), unabhängig davon, ob das Profil sich im Kinder- oder bereits im Erwachsenen-Interface befindet.

## 17. PDF-Export / Bericht [Beide]

Premium-Export als strukturierte Übersicht – getrackte Faktoren als kombinierte Graphen (mehrere Zeitverläufe übereinandergelegt, wie in Abschnitt 14), mit sichtbaren Markierungen für Medikamenten-/Dosiswechsel auf der Zeitachse (rein zeitlich/beschreibend, keine behauptete Kausalität). Muss gut versendbar sein (z. B. per E-Mail) – harte Anforderung, kein Nice-to-have.

Soft-Phrasing-Pflicht: endet immer mit einem Hinweis wie „Diese Darstellung zeigt persönliche Datenmuster und ersetzt keine medizinische Bewertung."

## 18. Backup, Datenportabilität & Export [Beide]

- Verschlüsselte Backups, mögliche Speicherorte iCloud/Google Drive – eigene, private Cloud der Person.
- 2-Datei-Redundanz-System (backup_a / backup_b), wöchentliches Auto-Backup.
- Sichtbarer „Von Backup wiederherstellen"-Flow in der App. Im aktuellen Prototyp existiert bislang nur ein einfacher Backup-Schalter + Export-Button, weder die 2-Datei-Redundanz noch ein sichtbarer Wiederherstellen-Flow – bekannte Abweichung (Abschnitt 24). Freiwillig: Schalter für Automatisierung wenn gewollt. Wenn nicht gewollt, müssen die Nutzer:innen gewarnt werden, dass die Daten dann bei Verlust des Handys nicht wiederhergestellt werden können.
- Daten müssen herunterladbar und auf ein anderes Gerät übertragbar sein – relevant auch, wenn ein Kind später ein eigenes Gerät bekommt. Kurze Info für Eltern bei Kinderversion.
- Nutzer:innen können: Daten exportieren, Daten löschen, Backups verwalten, Berechtigungen jederzeit ändern.

## 19. Premium-Modell / Monetarisierung [Beide]

- Kauf über den App-Store, keine eigene Server-/Kontolösung.
- Zielpreis-Kandidat: 6 €/Monat. Trial-Länge: 30 Tage.
- Basis-Version = Grundtracking bis zu drei Faktoren gleichzeitig, danach Premium.
- Premium sonst: Health-App-Import, erweiterte/interaktive Multi-Faktor-Graphen inkl. Wechsel-Marker, PDF-Berichte, CSV-Export, zusätzliche Module.
- Bei Minderjährigen (< 16, unabhängig von der UI-Stufe): Premium-Käufe erfordern die Eltern-PIN (Abschnitt 12). **Immer.**
- Trial-Umschalter im Prototyp rein simuliert, mit explizitem Hinweis, dass ein echter Kauf nur über App-/Play-Store laufen darf.

## 20. Barrierefreiheit [Beide]

Pflicht zum Launch. Basis-Accessibility von Anfang an: Schriftskalierung, Kontrast, Screenreader-Labels. Die farbenblind-sichere Diagramm-Darstellung (Farbe + Strichmuster + Punktform, Abschnitt 14) ist ein durchdachtes Detail, das so nirgends explizit gefordert war, aber gut zur Barrierefreiheits-Pflicht passt.

> Die im Text an anderer Stelle referenzierte vertiefte Prüfung der Consent-Verifizierungs-Alternativen für Minderjährige (Abschnitt 20 laut Querverweisen in Abschnitt 7/11/12) ist im Quelldokument nicht als eigener, ausformulierter Unterabschnitt enthalten, sondern in Abschnitt 12 („Consent & Recht") gebündelt – hier bewusst nicht ergänzt, um nichts zu erfinden.

## 21. Technische Architektur [Beide]

- Speicherung: SQLite lokal, Local-First.
- Sicherheit: FaceID, Fingerprint, Geräteauthentifizierung.
- Mindest-OS-Version: noch nicht final. Empfehlung: iOS 16/17 und Android 10 (API 29) – mit Dev-Team final gegenzuchecken.
- Zielbild der ersten Version (Demo/Investoren-Build vs. geschlossene Beta vs. store-fertiges Release) noch offen.

## 22. Datenmodell (Prototyp-„State") [Beide]

Sprache, Dark-Mode, Name, Geburtsdatum, Größe, Gewicht, Geschlecht, Fokus-Bereiche, Nutzungsgrund, Medikamentenstatus, Zyklus-Opt-in, hormoneller Status, Hormone-Opt-in, Health-Sync-Flag, Kids-Modus-Flag + Altersstufe, Name/Status der einwilligenden Person, Eltern-PIN-Status, Modul-Zustand (jetzt 10 Module: die ursprünglichen acht plus Ernährung und Libido, plus Schule bzw. Arbeit/Uni), Tageswerte, Medikamentenliste, Tages-Tags, Tages-Log (nach Datum), aktive Quick-Track-Kategorie, Premium-Status + Trial-Resttage, Benachrichtigungs-Einstellungen, Insights-Anzeigezustand (Einzeln/Kombiniert, Zeitraum, Diagramm/Tabelle, gewählte Kombi-Module), Verlaufs-Zustand (Woche/Monat, Kalendermonat-Offset, ohne Monats-Obergrenze).

## 23. Design & Markenauftritt [Beide]

- Designer: Leo Lamprecht (Grafikdesign, Berlin), zuständig u. a. für Logo und Schrifttyp. Design noch nicht final.
- Farbwelt bestätigt: Blau, Beige/Sand, reduziert, mit „Farbklecksen". Eigenschaften: warm, ruhig, modern, vertrauensvoll.
- Dark Mode: optional, nutzerwählbar.
- Erwachsenenversion: keine Emojis, nirgendwo.
- Kinderversion: ansprechend gestaltet, Richtung Plan-Toys-Stil, genderneutral, kindlich aber schlicht – entschieden: keine echten Unicode-Emoji-Zeichen, stattdessen eigens gestaltete Illustrationen/Icons (Abschnitt 5, 6).
- Kinder-Interface-Entwurf basiert auf einem eigenen SVG-Diskussionsentwurf, ausdrücklich „kein Ersatz für Leo Lamprechts Designarbeit", nur Diskussionsgrundlage.
- Offen: ob Onboarding eine Szene-/Charakter-Illustration bekommt (Beispielskizze bereits gezeigt) oder beim Icon-Level bleibt (Abschnitt 27).

---

*Abschnitte 24 ("bekannte Prototyp-Abweichungen") und 27 ("offene Punkte") werden im Quelldokument mehrfach referenziert, ihr Volltext lag für dieses Dokument nicht vor. Die referenzierten Einzelpunkte (z. B. Emoji-Nutzung im Prototyp, Range-Slider statt Zahlen-Kacheln, Health-Sync für alle statt nur Erwachsene, fehlende 2-Datei-Backup-Redundanz, offener PIN-Vergabe-Flow, offener Wortlaut der 16-Jahre-Checkbox) sind an den jeweiligen Stellen oben inline erhalten, anstatt hier einen nicht vorliegenden Volltext zu erfinden.*
