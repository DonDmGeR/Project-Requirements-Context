\# \*\*Vorlage für ein Project Requirements Roadmap (PRR)\*\*



Dies ist eine dynamische Übersicht, die den Status und die Priorisierung der einzelnen Anforderungen widerspiegelt, die aus dem PRD abgeleitet wurden. Sie dient als Leitfaden für den Project- und Technologie-Orchestrator, um die PRPs zu generieren und an die spezialisierten KI-Sub-Agenten zu verteilen.



---



\## \*\*1. Überblick und Gesamtstatus\*\*



Ein kurzer Abschnitt, der den aktuellen Status des Gesamtprojekts zusammenfasst und einen schnellen Überblick über den Fortschritt bietet.



\*\*Vorschlag für Inhalte:\*\*



\- \*\*Projektname:\*\* (z.B. „Automatische Erdnussbutter-Marmelade-Sandwich-Maschine“)

\- \*\*Version des PRD:\*\* (z.B. „v1.0“)

\- \*\*Letzte Aktualisierung der PRR:\*\* (Automatisch generiertes Datum)

\- \*\*Gesamtfortschritt:\*\* (z.B. „75 % der Anforderungen implementiert und getestet“)

\- \*\*Nächste Schritte:\*\* (Kurze Zusammenfassung der anstehenden Aufgaben)



---



\## \*\*2. Epics/Features Übersicht\*\*



Dieser Abschnitt listet die logischen, atomaren Einheiten oder Epics/Features auf, die du aus dem PRD extrahiert hast. Hier wird der Status auf höherer Ebene verfolgt.



\*\*Vorschlag für Inhalte (Tabelle):\*\*



| Epic/Feature Name      | Beschreibung                                        | Abhängigkeiten (von)               | Status        | Zugewiesener Agent (initial) | Anmerkungen                           |

| :--------------------- | :-------------------------------------------------- | :--------------------------------- | :------------ | :--------------------------- | :------------------------------------- |

| Benutzerauthentifizierung | Implementierung der Login- und Registrierungsfunktion. | -                                 | Abgeschlossen | Auth-Agent                   | Basis für andere Funktionen.           |

| Projectdarstellung     | Anzeige der Sandwich-Typen und Konfigurationsoptionen. | -                                 | In Arbeit     | UI-Agent                     | Benötigt Daten vom Schema-Agenten.     |

| Bestellabwicklung      | Prozess zur Erfassung und Verarbeitung von Bestellungen. | Benutzerauthentifizierung, Projectdarstellung | Ausstehend | Backend-Agent                | Kann erst starten, wenn Abhängigkeiten erfüllt sind. |

| ...                    | ...                                                 | ...                               | ...           | ...                           | ...                                     |



\*\*Erläuterungen:\*\*



\- \*\*Status:\*\* Kann z. B. „Ausstehend“, „In Arbeit“, „Zur Überprüfung“, „Fehlerhaft“, „Abgeschlossen“ sein.

\- \*\*Abhängigkeiten:\*\* Wichtig für die Priorisierung der PRP-Generierung.

\- \*\*Zugewiesener Agent (initial):\*\* Primär verantwortlicher KI-Sub-Agent.



---



\## \*\*3. Detaillierte PRP-Tracking (Pro Epic/Feature)\*\*



Für jedes Epic/Feature wird ein eigener Abschnitt erstellt, der die einzelnen PRPs und deren Status detailliert darstellt.



\*\*Vorschlag für Inhalte (für jedes Epic/Feature):\*\*



\### \*\*3.1. \[Epic/Feature Name]\*\*



\- \*\*Beschreibung:\*\* Detailliertere Beschreibung des Epics/Features aus dem PRD.

\- \*\*Priorität:\*\* (z.B. „Hoch“, „Mittel“, „Niedrig“)

\- \*\*PRD-Referenz:\*\* Verweis auf den genauen Abschnitt im PRD (z.B. „PRD Abschnitt 4.2 – Bestellabwicklung“).



\*\*Tabelle der zugehörigen PRPs:\*\*



| PRP ID    | Aufgabenbeschreibung (Kurz)               | Ziel-Sub-Agent | Status      | Feedback/Ergebnis (Kurz)     | Iterationen | Nächster Schritt/Aktion      |

| :-------- | :---------------------------------------- | :-------------- | :---------- | :--------------------------- | :---------- | :--------------------------- |

| ORDER-001 | Erstelle SQL-Schema für `orders` Tabelle. | Schema-Agent    | Abgeschlossen | Schema erfolgreich generiert. | 1           | COD-ORDER-001 generieren     |

| ORDER-002 | Implementiere `/api/order` POST-Endpunkt. | Coding-Agent    | Fehlerhaft  | Validierungsfehler in Request-Body. | 2           | Bugfix PRP generiert (ORDER-003) |

| ORDER-003 | Fix: Validierung des Bestell-Request-Bodies. | Coding-Agent | In Arbeit   | -                             | 1           | -                             |

| ORDER-004 | Schreibe Unit-Tests für Bestell-API.      | Test-Agent      | Ausstehend  | -                             | 0           | Abhängig von COD-ORDER-002/003 |

| ...       | ...                                        | ...              | ...          | ...                           | ...         | ...                           |



\*\*Erläuterungen:\*\*



\- \*\*PRP ID:\*\* Eindeutige ID für jeden PRP.

\- \*\*Aufgabenbeschreibung:\*\* Kurze Zusammenfassung der Aufgabe.

\- \*\*Ziel-Sub-Agent:\*\* Zuständiger KI-Agent.

\- \*\*Status:\*\* Granular: z. B. „Generiert“, „Gesendet“, „In Bearbeitung“, „Erfolgreich“, „Fehlerhaft“, „Feedback erhalten“.

\- \*\*Feedback/Ergebnis:\*\* Knappes Ergebnis oder Feedback.

\- \*\*Iteration:\*\* Anzahl der Überarbeitungen.

\- \*\*Nächster Schritt/Aktion:\*\* Klarer nächster Handlungsschritt.



---



\## \*\*4. Abhängigkeitsgraph/Flussdiagramm (Optional, aber sehr nützlich)\*\*



Ein visueller Graph, der die Abhängigkeiten zwischen den Epics/Features und ggf. den einzelnen PRPs darstellt.



\*\*Vorteile:\*\*



\- Schnelle visuelle Erkennung von Engpässen.

\- Hilft dem Orchestrator bei der Planung der nächsten PRPs.



---



\## \*\*5. Technische Präferenzen und Einschränkungen (Global)\*\*



Globale technische Rahmenbedingungen aus dem PRD.



\*\*Beispiel:\*\*



\- \*\*Backend:\*\* Python/Flask

\- \*\*Datenbank:\*\* PostgreSQL

\- \*\*Frontend:\*\* HTML/CSS/JavaScript

\- \*\*Tests:\*\* Pytest

\- \*\*Benutzeroberfläche:\*\* 5″-Touchscreen, zwei Statusleuchten, Signalgeber

\- \*\*Hardware:\*\* FDM-3D-gedruckte Teile, handelsübliche Bauteile, Eigenentwicklung Steuerplatine



---



\## \*\*6. Offene Punkte / Forschungsbedarf\*\*



Bereich für offene Fragen oder Klärungsbedarf.



\*\*Beispiele:\*\*



\- „Klärung: Genaues Format für die Viskositäts- und Dickenmessdaten von der Steuerplatine.“

\- „Offen: Kommunikationsprotokoll zwischen Steuerplatine und Backend?“



---



\## \*\*7. Änderungsverlauf\*\*



Chronologische Nachverfolgung der Änderungen.



| Datum     | Version | Beschreibung der Änderung                          |

| :-------- | :------ | :------------------------------------------------- |

| 2025-07-11 | 1.0     | Erste Version basierend auf PRD v1.0.              |

| 2025-07-12 | 1.1     | Aktualisierung der PRP-Status nach erster Agentenrunde. |

