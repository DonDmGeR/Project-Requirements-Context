**# \*\*Vorlage für ein Product Requirement Document (PRD)\*\***



**Dies ist die Standardvorlage für ein \*\*Product Requirement Document (PRD)\*\*.**



**Das Ziel eines PRDs ist es, \*\*klar und umfassend zu definieren, was ein Produkt sein soll\*\*. Es dient als \*\*primäre Referenzquelle\*\* für den gesamten Entwicklungszyklus. Die Erstellung eines PRDs stellt sicher, dass:**



**1.  Das zu entwickelnde Produkt einen \*\*klaren Bedarf\*\* erfüllt und vermarktbar ist.**

**2.  Das gesamte Team – einschließlich des \*\*Produkt- und Technologie-Orchestrators\*\* und der KI-Agenten – ein \*\*gemeinsames, konsistentes Verständnis\*\* vom Produkt hat.**

**3.  Alle nachfolgenden \*\*Product Requirement Prompts (PRPs)\*\* und die \*\*Product Requirements Roadmap (PRR)\*\* direkt und nachvollziehbar aus den hier definierten Anforderungen abgeleitet werden können.**



**Alle Beispiele hier beziehen sich auf eine \*\*theoretische Android Handy Gewohnheiten Tracking App\*\*.**



**-----**



**## \*\*Überblick\*\***



**Eine prägnante Beschreibung dessen, was wir bauen wollen. Dieser Abschnitt fasst die Essenz des Produkts und seine übergeordnete Vision zusammen und bildet die Grundlage für die initiale \*\*Epic/Feature-Identifizierung in der PRR\*\*.**



**\*\*Beispiel:\*\***



**> Dieses PRD beschreibt die Entwicklung einer \*\*Android-App zum Tracking und zur Förderung positiver Gewohnheiten\*\*.**

**>**

**> Die übergeordnete Vision ist es, ein \*\*intuitives und motivierendes Tool\*\* zu schaffen, das Nutzern hilft, neue Gewohnheiten aufzubauen, bestehende zu pflegen und ihren Fortschritt visuell zu verfolgen, um ein gesünderes und produktiveres Leben zu führen.**



**-----**



**## \*\*Ziele\*\***



**Konkrete Beschreibungen der Fähigkeiten, die das Produkt besitzen muss. Diese Ziele sollten so spezifisch wie möglich sein, ohne bereits technische Details vorwegzunehmen. Sie sind entscheidend für die Ableitung von \*\*PRPs\*\* und die Definition der \*\*Akzeptanzkriterien\*\* für Epics/Features in der \*\*PRR\*\*.**



**\*\*Beispiel:\*\***



**>   \* Ermöglichen des \*\*Erstellens, Bearbeitens und Löschens\*\* von individuellen Gewohnheiten.**

**>   \* Bereitstellung einer einfachen Möglichkeit, Gewohnheiten als \*\*erledigt zu markieren\*\*.**

**>   \* Anzeige des \*\*Fortschritts von Gewohnheiten\*\* über Zeit (z.B. Streak-Anzeige, Kalenderansicht).**

**>   \* Implementierung von \*\*anpassbaren Erinnerungen\*\* für jede Gewohnheit.**

**>   \* Gewährleistung einer \*\*intuitiven und benutzerfreundlichen Oberfläche\*\* auf Android-Geräten.**

**>   \* Unterstützung der \*\*Offline-Nutzung\*\* und Synchronisierung bei Online-Verbindung.**



**-----**



**## \*\*Nicht-Ziele\*\***



**Eine klare Abgrenzung dessen, was das Produkt \*\*nicht\*\* leisten muss. Dies ist essenziell, um den Projektumfang zu kontrollieren und hilft dem Orchestrator, unnötige \*\*PRPs\*\* zu vermeiden und den Fokus zu wahren.**



**\*\*Beispiel:\*\***



**>   \* Keine sozialen Funktionen oder Teilen von Gewohnheiten mit anderen Nutzern in der Initialversion.**

**>   \* Keine Integration mit externen Fitness-Trackern oder Gesundheits-Apps.**

**>   \* Keine plattformübergreifende Unterstützung (fokussiert ausschließlich auf Android).**

**>   \* Keine komplexen Analysen oder KI-basierte Empfehlungen für Gewohnheiten in der ersten Version.**



**-----**



**## \*\*Zielgruppe\*\***



**Ein Abschnitt, der detailliert beschreibt, \*\*für wen\*\* das Produkt gedacht ist, welche Erwartungen sie haben und wie sie mit dem Produkt interagieren möchten. Diese Informationen sind grundlegend für die Formulierung der \*\*User Stories\*\* innerhalb der \*\*PRPs\*\* und zur Sicherstellung der \*\*Nutzerzentrierung\*\* der Lösungen.**



**\*\*Beispiel:\*\***



**> Die Hauptzielgruppe dieser App sind \*\*Einzelpersonen, die ihre Produktivität steigern, schlechte Gewohnheiten ablegen oder neue, positive Routinen etablieren möchten\*\*. Sie sind motiviert, ihre Fortschritte zu sehen und benötigen eine einfache, aber effektive Möglichkeit, ihre Gewohnheiten zu verfolgen.**

**>**

**> Sie sind in der Regel \*\*Android-Nutzer\*\*, die Wert auf eine saubere Benutzeroberfläche und zuverlässige Funktionen legen. Sie sind offen für digitale Tools zur Selbstverbesserung, aber möglicherweise keine Technik-Experten.**



**-----**



**## \*\*Bestehende Lösungen und Probleme\*\***



**Dieser Abschnitt analysiert vorhandene Alternativen und deren Schwächen, um die Notwendigkeit und den Mehrwert des neuen Produkts zu begründen. Diese Erkenntnisse können in \*\*PRPs\*\* einfließen, um bekannte Fallstricke zu vermeiden oder spezifische Wettbewerbsvorteile zu implementieren.**



**\*\*Beispiel:\*\***



**> Es gibt zahlreiche Gewohnheiten-Tracking-Apps auf dem Markt, aber viele haben Schwächen:**

**>**

**>   \* \*\*"HabitMaster"\*\*: Zu komplex, überladen mit Funktionen, die die Kernaufgabe erschweren.**

**>   \* \*\*"SimpleTrack"\*\*: Zu minimalistisch, bietet keine ausreichenden Visualisierungen oder Anpassungsmöglichkeiten für Erinnerungen.**

**>   \* \*\*"DailyRoutine"\*\*: Veraltete Benutzeroberfläche, schlechte Performance auf älteren Geräten.**

**>   \* \*\*Fehlende Offline-Fähigkeit:\*\* Viele Apps erfordern eine ständige Internetverbindung, was die Nutzung in bestimmten Szenarien einschränkt.**



**-----**



**## \*\*Annahmen\*\***



**Annahmen über Nutzerverhalten, deren Situation und Erwartungen, die \*\*stets durch Kundeninterviews oder Daten belegt sein müssen\*\*. Diese Annahmen dienen als wichtige Randbedingungen für die \*\*PRP-Generierung\*\* und helfen dem Orchestrator, Prioritäten zu setzen.**



**\*\*Beispiel:\*\***



**>   \* Nutzer besitzen ein \*\*Android-Smartphone mit Android 8.0 (Oreo) oder neuer\*\*.**

**>   \* Nutzer sind bereit, der App \*\*Benachrichtigungsberechtigungen\*\* zu erteilen, um Erinnerungen zu erhalten.**

**>   \* Die meisten Gewohnheiten werden \*\*täglich oder wöchentlich\*\* verfolgt, nicht stündlich.**

**>   \* Nutzer bevorzugen eine \*\*visuelle Darstellung ihres Fortschritts\*\* (z.B. farbige Kalender, Streaks).**

**>   \* Die App wird primär für \*\*persönliche Gewohnheiten\*\* genutzt, nicht für Team- oder Gruppen-Tracking.**



**-----**



**## \*\*Einschränkungen\*\***



**Grundlegende, oft technische, Anforderungen und Rahmenbedingungen für die Implementierung. Diese Einschränkungen sind essenziell für die \*\*technischen Präferenzen und Einschränkungen in der PRR\*\* und müssen in jedem relevanten \*\*PRP\*\* berücksichtigt werden.**



**\*\*Beispiel:\*\***



**> Die App muss unter Einhaltung folgender technischer Einschränkungen entwickelt werden:**

**>**

**>   \* \*\*Plattform:\*\* Native Android-Entwicklung (Kotlin/Java).**

**>   \* \*\*Datenbank:\*\* Lokale Speicherung der Gewohnheitsdaten auf dem Gerät.**

**>   \* \*\*Benachrichtigungen:\*\* Nutzung des Android Notification Systems für Erinnerungen.**

**>   \* \*\*Performance:\*\* Flüssige UI-Animationen und schnelle Ladezeiten, auch bei vielen Gewohnheiten.**

**>   \* \*\*Batterieverbrauch:\*\* Optimierung für minimalen Batterieverbrauch im Hintergrund.**

**>   \* \*\*Datenschutz:\*\* Alle Nutzerdaten bleiben lokal auf dem Gerät des Nutzers.**



**-----**



**## \*\*Zentrale Anwendungsfälle\*\***



**Alle Situationen und Gründe, aus denen Benutzer mit dem Produkt interagieren. Dies sind die Kernaufgaben, die das Produkt erfüllen muss. Jeder Anwendungsfall wird in der \*\*PRR\*\* als Epic/Feature getrackt und führt zu einer Reihe detaillierter \*\*PRPs\*\*.**



**\*\*Beispiel:\*\***



**>   \* \*\*Gewohnheit erstellen:\*\* Ein Nutzer kann eine neue Gewohnheit mit Name, Häufigkeit und optionaler Erinnerung hinzufügen.**

**>   \* \*\*Gewohnheit als erledigt markieren:\*\* Ein Nutzer kann eine Gewohnheit für den aktuellen Tag als erledigt abhaken.**

**>   \* \*\*Fortschritt einer Gewohnheit ansehen:\*\* Ein Nutzer kann eine Übersicht über seinen Fortschritt für eine spezifische Gewohnheit sehen (z.B. Streak, Kalenderansicht).**

**>   \* \*\*Erinnerungen erhalten:\*\* Der Nutzer wird zu den festgelegten Zeiten an seine Gewohnheiten erinnert.**



**Für jeden Anwendungsfall sollte es einen detaillierten Abschnitt geben, wie das Produkt diesen umsetzt. Diese detaillierten Beschreibungen sind die direkte Basis für die \*\*Spezifikationen in den PRPs\*\*.**



**\*\*Beispiel:\*\***



**> ### \*\*Gewohnheit erstellen und speichern\*\***

**>**

**> Dieser Anwendungsfall beschreibt die Kernfunktionalität zur Erfassung und Persistenz von Gewohnheitsdaten.**

**>**

**> \*\*Funktionale Anforderungen:\*\***

**>**

**>   \* \*\*UI-Flow:\*\* Der Nutzer navigiert zu einem "Neue Gewohnheit erstellen"-Bildschirm, gibt einen Namen ein (Pflichtfeld), wählt eine Häufigkeit (Täglich, Wöchentlich, Bestimmte Tage), und kann optional eine Erinnerungszeit festlegen. Nach dem Speichern wird die Gewohnheit in der Hauptübersicht angezeigt.**

**>   \* \*\*Datenmodell:\*\* Eine Gewohnheit muss mindestens folgende Attribute haben: `id` (UUID), `name` (String), `frequency\\\_type` (Enum: DAILY, WEEKLY, CUSTOM), `custom\\\_days` (Liste von Wochentagen, falls `CUSTOM`), `reminder\\\_time` (Zeitformat, optional), `creation\\\_date` (Datum).**

**>   \* \*\*Validierung:\*\* Der Gewohnheitsname darf nicht leer sein. Erinnerungszeiten müssen gültige Uhrzeiten sein.**

**>   \* \*\*Speicherung:\*\* Die Gewohnheit muss \*\*persistent lokal auf dem Gerät gespeichert\*\* werden, sodass sie auch nach dem Schließen der App verfügbar ist.**

**>**

**> \*\*Nicht-funktionale Anforderungen:\*\***

**>**

**>   \* Der Speichervorgang muss \*\*asynchron\*\* erfolgen, um die UI nicht zu blockieren.**

**>   \* Die Datenintegrität muss bei der Speicherung gewährleistet sein.**

**>   \* Die App muss auch \*\*offline\*\* neue Gewohnheiten erstellen können.**



**-----**



**## \*\*Forschung\*\***



**Dieser Abschnitt fasst alle Forschungsfragen zusammen, die zur Erstellung des PRD beigetragen haben. \*\*Er muss abgeschlossen sein, bevor das PRD geschrieben wird\*\*, da er die gesamte Produktdefinition untermauert. Die hier gewonnenen Erkenntnisse sind entscheidend für die \*\*Priorisierung\*\* in der \*\*PRR\*\* und die \*\*detaillierten Spezifikationen\*\* in den \*\*PRPs\*\*.**



**### \*\*Nutzerforschung\*\***



**Dieser Teil liefert den Großteil der Grundlage für das PRD. Er sollte in Form einiger Schlüsselfragen aufgebaut sein, die als Überschriften dienen, darunter jeweils die Antwort basierend auf der Forschung. Der ganze Abschnitt sollte Links zu Interview-Notizen enthalten.**



**\*\*Beispiel:\*\***



**> ### Welche Art von Erinnerungen sind für Nutzer am effektivsten?**

**>**

**> Aus \[Nutzerinterviews](https://www.google.com/search?q=) und \[Umfragen zu Gewohnheiten-Apps](https://www.google.com/search?q=) geht hervor, dass \*\*anpassbare, zeitbasierte Erinnerungen\*\* (z.B. "Erinnere mich um 8:00 Uhr an 'Sport'") am wichtigsten sind. Eine Studie \[siehe: Studie zu Benachrichtigungseffektivität](https://www.google.com/search?q=) zeigt, dass zu viele oder zu wenige Erinnerungen die Motivation negativ beeinflussen. Die Möglichkeit, Erinnerungen pro Gewohnheit zu aktivieren/deaktivieren und die Uhrzeit frei zu wählen, ist entscheidend.**

**>**

**> ### Welche Visualisierungen motivieren Nutzer am stärksten?**

**>**

**> \[Feedback-Sitzungen mit potenziellen Nutzern](https://www.google.com/search?q=) haben gezeigt, dass eine \*\*"Streak"-Anzeige\*\* (fortlaufende Tage, an denen eine Gewohnheit erledigt wurde) und eine \*\*Kalenderansicht\*\*, die erledigte Tage farblich hervorhebt, die beliebtesten und motivierendsten Visualisierungen sind. Eine einfache Fortschrittsleiste für wöchentliche Gewohnheiten ist ebenfalls gewünscht.**



**-----**



**### \*\*Technische Forschung\*\***



**Dieser Teil beschreibt grob, wie das Produkt gebaut wird. Mathematische Berechnungen, Komponentenrecherche oder erste Prototypen können erforderlich sein, um diesen Abschnitt zu vervollständigen. Die hierin enthaltenen technischen Entscheidungen fließen direkt in die \*\*technischen Spezifikationen der PRPs\*\* und die \*\*globalen technischen Einschränkungen in der PRR\*\* ein.**



**\*\*Beispiel:\*\***



**> ### Welche lokale Datenbanklösung ist für Android-Gewohnheitsdaten am besten geeignet?**

**>**

**> Eine Untersuchung gängiger Android-Datenbanken wie SQLite (mit Room ORM), Realm und ObjectBox \[siehe: Vergleich lokaler Android-DBs](https://www.google.com/search?q=) hat ergeben, dass \*\*Room mit SQLite\*\* die beste Wahl für unsere Anforderungen ist. Es bietet eine ausgezeichnete Abstraktionsschicht, compile-time SQL-Validierung und ist gut in das Android-Ökosystem integriert. Dies ist entscheidend für den \*\*Schema-Agenten-PRP\*\* zur Definition des Datenmodells und für den \*\*Coding-Agenten-PRP\*\* zur Implementierung der Datenpersistenz.**

**>**

**> ### Wie können Hintergrundaufgaben für Erinnerungen effizient und zuverlässig implementiert werden?**

**>**

**> Die Analyse von Android-Hintergrundverarbeitungsmechanismen \[siehe: Android Background Processing Guide](https://www.google.com/search?q=) zeigt, dass \*\*WorkManager\*\* die robusteste und von Google empfohlene Lösung für planbare, persistente Hintergrundaufgaben ist, wie z.B. das Senden von Erinnerungen. Alternativen wie `AlarmManager` sind weniger flexibel bei Doze-Modus und App-Standby. Die Entscheidung für WorkManager wird direkt in die \*\*Coding-Agenten-PRPs\*\* für die Erinnerungsfunktionalität einfließen.**



**-----**

