## 📌 **Vorlage für ein Project Requirement Document (PRD)**

---

**Dies ist die Standardvorlage für ein Project Requirement Document (PRD).**

Ein PRD hat das Ziel, **klar und umfassend zu definieren, was ein Produkt leisten soll**. Es dient als **primäre Referenzquelle** für den gesamten Entwicklungszyklus. Die Erstellung stellt sicher, dass:

1. Das zu entwickelnde Produkt einen **klaren Bedarf erfüllt** und vermarktbar ist.
2. Das gesamte Team – einschließlich des **Produkt- und Technologie-Orchestrators** sowie der KI-Agenten – ein **gemeinsames, konsistentes Verständnis** des Produkts hat.
3. Alle nachfolgenden **Project Requirement Prompts (PRPs)** und die **Project Requirements Roadmap (PRR)** direkt und nachvollziehbar aus den hier definierten Anforderungen abgeleitet werden können.

> **Beispiel:**
> Alle Beispiele hier beziehen sich auf eine **theoretische Android-App zum Tracking und zur Förderung positiver Gewohnheiten**.

---

## ✅ **Überblick**

Eine prägnante Beschreibung dessen, **was entwickelt werden soll**. Dieser Abschnitt fasst die Essenz des Produkts und seine übergeordnete Vision zusammen und bildet die Grundlage für die initiale **Epic-/Feature-Identifizierung in der PRR**.

**Beispiel:**

> Dieses PRD beschreibt die Entwicklung einer **Android-App zum Tracking und zur Förderung positiver Gewohnheiten**.
> Die übergeordnete Vision ist es, ein **intuitives und motivierendes Tool** zu schaffen, das Nutzer unterstützt, neue Gewohnheiten aufzubauen, bestehende zu pflegen und ihren Fortschritt visuell zu verfolgen, um ein gesünderes und produktiveres Leben zu führen.

---

## 🎯 **Ziele**

Konkrete Beschreibungen der **Fähigkeiten**, die das Produkt besitzen muss. Diese Ziele sollten **spezifisch** sein, ohne technische Details vorwegzunehmen. Sie sind entscheidend für die Ableitung von **PRPs** und die Definition der **Akzeptanzkriterien** in der **PRR**.

**Beispiel:**

* Erstellen, Bearbeiten und Löschen individueller Gewohnheiten.
* Einfache Möglichkeit, Gewohnheiten als **erledigt** zu markieren.
* Anzeige des **Fortschritts** (z. B. Streaks, Kalenderansicht).
* Anpassbare **Erinnerungen** pro Gewohnheit.
* **Intuitive, benutzerfreundliche Oberfläche** auf Android-Geräten.
* Unterstützung der **Offline-Nutzung** und Synchronisierung bei Verbindung.

---

## ❌ **Nicht-Ziele**

Eine klare Abgrenzung dessen, was das Produkt **nicht leisten muss**. Diese Liste schützt den Projektumfang und hilft dem Orchestrator, überflüssige **PRPs** zu vermeiden.

**Beispiel:**

* Keine sozialen Funktionen oder Sharing in der Initialversion.
* Keine Integration mit externen Fitness-Trackern oder Gesundheits-Apps.
* Keine plattformübergreifende Unterstützung (nur Android).
* Keine komplexen Analysen oder KI-basierten Empfehlungen in Version 1.

---

## 👥 **Zielgruppe**

Für wen ist das Produkt gedacht? Welche Erwartungen haben diese Nutzer, und wie interagieren sie mit dem Produkt? Diese Informationen sind grundlegend für die **User Stories** in den **PRPs**.

**Beispiel:**

> Die Hauptzielgruppe sind **Einzelpersonen**, die ihre Produktivität steigern, schlechte Gewohnheiten ablegen oder neue Routinen etablieren wollen.
> Sie legen Wert auf eine **übersichtliche UI**, sind Android-Nutzer und meist keine Technik-Experten, aber offen für digitale Tools zur Selbstoptimierung.

---

## 🔍 **Bestehende Lösungen & Probleme**

Analyse vorhandener Alternativen, deren Schwächen und die daraus abgeleitete **Daseinsberechtigung** der eigenen Lösung. Erkenntnisse hieraus fließen in **PRPs** ein.

**Beispiel:**

> * **HabitMaster:** Zu komplex, überladen.
> * **SimpleTrack:** Zu minimalistisch, kaum Visualisierungen oder flexible Erinnerungen.
> * **DailyRoutine:** Veraltete Oberfläche, schlechte Performance.
> * **Offline-Fähigkeit:** Viele Apps benötigen ständige Internetverbindung.

---

## ⚙️ **Annahmen**

Zentrale Annahmen über Nutzerverhalten oder technische Gegebenheiten, die durch Daten oder Interviews abgesichert sein müssen. Sie bilden wichtige Randbedingungen für **PRPs**.

**Beispiel:**

* Nutzer verwenden Android 8.0 oder neuer.
* Sie gewähren Benachrichtigungsberechtigungen.
* Gewohnheiten werden überwiegend **täglich oder wöchentlich** verfolgt.
* Nutzer bevorzugen **visuelle Fortschrittsanzeigen**.
* Die App wird **nur für persönliche Nutzung** eingesetzt.

---

## 🛠️ **Einschränkungen**

Technische und rechtliche Rahmenbedingungen, die bei der Implementierung unbedingt beachtet werden müssen.

**Beispiel:**

* **Plattform:** Native Android-Entwicklung (Kotlin/Java).
* **Datenbank:** Lokale Speicherung auf dem Gerät.
* **Benachrichtigungen:** Android Notification System.
* **Performance:** Schnelle Ladezeiten, flüssige UI.
* **Batterie:** Minimaler Verbrauch im Hintergrund.
* **Datenschutz:** Daten bleiben lokal.

---

## 🔑 **Zentrale Anwendungsfälle**

Alle Kernaufgaben, die das Produkt erfüllen muss. Jeder Anwendungsfall wird später als **Epic/Feature** in der **PRR** erfasst und in spezifischen **PRPs** detailliert.

**Beispiel:**

* **Gewohnheit erstellen:** Mit Name, Häufigkeit, optionaler Erinnerung.
* **Erledigen:** Gewohnheit für den Tag abhaken.
* **Fortschritt ansehen:** Streaks, Kalenderansicht.
* **Erinnerung erhalten:** Zeitbasierte Notifications.

**Beispiel-Detail:**

### **Gewohnheit erstellen & speichern**

**Funktional:**

* UI-Flow: Nutzer öffnet „Neue Gewohnheit“, gibt Name ein (Pflichtfeld), wählt Häufigkeit, optional Erinnerung.
* Datenmodell: `id` (UUID), `name` (String), `frequency_type` (Enum), `custom_days` (Liste), `reminder_time` (optional), `creation_date`.
* Validierung: Name darf nicht leer sein, Zeiten müssen gültig sein.
* Speicherung: Persistente lokale Speicherung.

**Nicht-funktional:**

* Speichern asynchron.
* Datenintegrität gewährleisten.
* Auch offline nutzbar.

---

## 📚 **Forschung**

Die Forschung liefert die Basis für alle **Anforderungen, PRPs und Priorisierungen**. Sie sollte abgeschlossen sein, bevor das PRD finalisiert wird.

### **Nutzerforschung**

**Beispiel:**

* **Welche Erinnerungen sind effektiv?**
  Interviews & Umfragen zeigen: **zeitbasierte, frei konfigurierbare Erinnerungen** sind entscheidend.
* **Welche Visualisierung motiviert?**
  Nutzer bevorzugen **Streaks**, Kalender und Fortschrittsleisten.

### **Technische Forschung**

**Beispiel:**

* **Lokale Datenbank:** Room/SQLite ist am geeignetsten (stabil, bekannt, gut dokumentiert).
* **Hintergrundaufgaben:** WorkManager ist der Standard für planbare, persistente Tasks.

---

## ✔️ **Fertig**

Mit dieser Vorlage kannst du **sofort spezifische PRPs und die PRR ableiten**. Jede Anpassung sollte **im PRD nachvollziehbar dokumentiert** werden. 
