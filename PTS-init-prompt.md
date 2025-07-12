# **Vorlage für eine Project Technical Specification (PTS)**

Dies ist die Standardvorlage für eine **Project Technical Specification (PTS)**.

Das Ziel einer PTS ist es, **die technischen Grundlagen und Richtlinien für die Implementierung eines Projekts klar und umfassend zu definieren**. Sie dient als **zentrale technische Referenzquelle** für den gesamten Entwicklungszyklus und ergänzt das Project Requirement Document (PRD), indem sie das *Wie* der Umsetzung detailliert beschreibt.

Die Erstellung einer PTS stellt sicher, dass:

1. Die gewählte **Architektur und das technische Design** den Projektanforderungen und langfristigen Zielen entsprechen.
2. Das gesamte Entwicklungsteam – einschließlich des **Project- und Technologie-Orchestrators** und der spezialisierten KI-Agenten – ein **gemeinsames, konsistentes Verständnis** der technischen Umsetzung hat.
3. KI-Agenten Code generieren, der **architektonisch korrekt, stilistisch konsistent und den Best Practices** des Projekts entspricht.
4. Die **Project Requirements Roadmap (PRR)** mit den notwendigen technischen Kontexten für die Planung und das Tracking angereichert wird.

Alle Beispiele hier beziehen sich auf die **theoretische Android Handy Gewohnheiten Tracking App**.

---

## **1. Überblick und Technische Vision**

Ein prägnanter Abschnitt, der die übergeordnete technische Vision zusammenfasst und die wichtigsten architektonischen Prinzipien vorstellt.

**Inhalte:**

- **Projektname:** (z. B. *Android Habit Tracker App*)
- **Version des PRD:** (z. B. *v1.0*)
- **Version der PTS:** (z. B. *v1.0 – Initiales Technisches Design*)
- **Letzte Aktualisierung der PTS:** (automatisch generiertes Datum)
- **Technische Vision:** (kurze Zusammenfassung der angestrebten technischen Qualität und Ziele)

**Beispiel:**

> Diese PTS legt die technische Architektur und die Entwicklungsrichtlinien für die Android Habit Tracker App fest. Unsere technische Vision ist es, eine **performante, wartbare und erweiterbare native Android-Anwendung** zu entwickeln, die eine exzellente Nutzererfahrung bietet und auf einer **robusten, modularen Codebasis** aufbaut. Der Fokus liegt auf Offline-Fähigkeit und minimalem Batterieverbrauch.

---

## **2. Architekturprinzipien und -muster**

Dieser Abschnitt definiert die grundlegenden architektonischen Prinzipien und Design-Muster, die im gesamten Projekt angewendet werden sollen.

**Inhalte:**

- **Hauptarchitekturmuster:** (z. B. MVVM, Clean Architecture)
- **Modulstruktur:** (logische/physische Module)
- **Abhängigkeitsmanagement:** (z. B. Dependency Injection)
- **Fehlerbehandlung:** (globale Strategien)
- **Teststrategie:** (Unit-, Integrations-, UI-Tests)

**Beispiel:**

- **Architekturmuster:** Die App folgt dem **MVVM (Model-View-ViewModel)**-Muster für klare Trennung von UI-Logik, Business-Logik und Datenzugriff. Zusätzlich wird ein **Repository-Pattern** verwendet.
- **Modulstruktur:** Module: `app` (UI), `data` (Persistenz), `domain` (Business-Logik).
- **Abhängigkeitsmanagement:** **Hilt (Dagger)** für Dependency Injection.
- **Fehlerbehandlung:** Zentrale `Result`- oder Sealed-Classes-Strategie, Logging über dediziertes Framework.
- **Teststrategie:** Fokus auf **Unit-Tests** für ViewModel/Repository, **Instrumented Tests** für UI und Persistenz.

---

## **3. Wichtige Architekturentscheidungen (ADRs)**

Hier werden Schlüsselfragen dokumentiert.

**Inhalte:**

- **ADR ID**
- **Titel**
- **Problem**
- **Entscheidung**
- **Begründung**
- **Konsequenzen** (optional)
- **Referenz**

**Beispiel:**

- **ADR ID:** ADR-001  
  **Titel:** Wahl der lokalen Datenbanklösung  
  **Problem:** Persistente lokale Speicherung notwendig.  
  **Entscheidung:** **Room Persistence Library (SQLite-basiert)**  
  **Begründung:** Compile-Time SQL-Validierung, Integration mit Kotlin Coroutines.  
  **Konsequenzen:** Entities, DAOs, Room-DB-Klasse nötig.  
  **Referenz:** [Link zu ADR-001.md]

- **ADR ID:** ADR-002  
  **Titel:** Hintergrundaufgaben für Erinnerungen  
  **Problem:** Erinnerungen müssen zuverlässig laufen.  
  **Entscheidung:** **Android WorkManager**  
  **Begründung:** Robust gegen Doze/Standby.  
  **Konsequenzen:** WorkRequests/Worker-Klassen definieren.  
  **Referenz:** [Link zu ADR-002.md]

---

## **4. Systemkomponenten und Interaktionen**

Detaillierte Beschreibung der Komponenten.

**Inhalte:**

- **Komponentenübersicht:** z. B. UI, ViewModel, Repository, DB, Notification Service
- **Datenflussdiagramme:** optional
- **Interne APIs:** Definition der Schnittstellen

**Beispiel:**

- **User Interface (UI):** Compose-basierte Activities/Fragments.
- **ViewModels:** Halten UI-State, verarbeiten Events.
- **Domain Layer:** Business-Logik.
- **Repository Layer:** Datenzugriff.
- **Local Database:** Room.
- **Notification Service:** WorkManager + Notifications.

**Beispiel-Datenfluss:**

1. Nutzer klickt „Erledigt“.
2. UI ruft ViewModel-Funktion auf.
3. ViewModel ruft Domain-Use-Case auf.
4. Use-Case nutzt Repository.
5. Repository aktualisiert Room-DB.
6. LiveData/Flow triggert Update.
7. UI wird neu gezeichnet.

---

## **5. Coding Standards und Style Guide**

Regeln für Codequalität.

**Inhalte:**

- **Sprache & Frameworks:** Kotlin, Compose.
- **Formatierung:** 4 Spaces, 120 Zeichen max.
- **Benennung:** PascalCase (Klassen), camelCase (Funktionen), SCREAMING_SNAKE_CASE (Konstanten).
- **Kommentare:** KDoc für öffentliche APIs, Inline-Kommentare für komplexe Logik.
- **Best Practices:**  
  - **Nullability:** Null-Safety strikt. Kein `!!` ohne Notwendigkeit.
  - **Coroutines:** Strukturierte Parallelität.
  - **Error Handling:** Result/Sealed Classes für erwartete Fehler.
  - **Logging:** `Timber` statt `println()`.
- **Linter:** `ktlint`/`detekt` Regeln verbindlich.

---

## **6. Sicherheits- und Performance-Richtlinien**

Grundregeln für Sicherheit & Performance.

**Inhalte:**

- **Datenschutz:** Daten lokal, verschlüsselt.
- **Sichere Codierung:** Input validieren, keine harten Secrets.
- **Performance:**  
  - UI-Updates im Main-Thread.
  - Lange Operationen in Coroutines.
