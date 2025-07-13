# **Project- und Technologie-Orchestrator System** 🚀

Dieses Repository enthält die Kernvorlagen und Richtlinien für unser **Project- und Technologie-Orchestrator System**, ein KI-gestütztes Framework zur effizienten und konsistenten Entwicklung von Softwareprojekten. Es wurde entwickelt, um die Lücke zwischen Projektvision und technischer Implementierung zu schließen, indem es den gesamten Prozess durch strukturierte Dokumentation und präzise KI-Anweisungen optimiert.

Unser System basiert auf vier zentralen Dokumenttypen, die miteinander synergetisch wirken:

1. **Project Requirement Details (PRD):** Definiert das *WAS* (Projektvision & Anforderungen).
2. **Project Technical Specification (PTS):** Definiert das *WIE* (Architektur & technische Richtlinien).
3. **Project Requirements Roadmap (PRR):** Trackt den *STATUS* (Priorisierung & Fortschritt).
4. **Project Requirement Prompt (PRP):** Generiert *AKTIONEN* (detaillierte Anweisungen für KI-Agenten).

---

## **1. Das System im Überblick**

Das Project- und Technologie-Orchestrator System ermöglicht eine **strukturierte, nachvollziehbare und KI-optimierte Projektentwicklung**. Es gewährleistet, dass alle Beteiligten – menschliche Teams und KI-Agenten – ein klares, konsistentes Verständnis des zu entwickelnden Projekts und seiner technischen Umsetzung haben.

**Kernmerkmale:**

* **Top-Down-Ansatz:** Beginnt mit der High-Level-Projektvision und destilliert diese schrittweise zu ausführbaren Aufgaben.
* **KI-gestützte Effizienz:** Optimiert die Übergabe von Anforderungen an spezialisierte KI-Agenten, um Code-Generierung, Schema-Design, Test-Erstellung und mehr zu automatisieren.
* **Qualitätssicherung durch Richtlinien:** Stellt sicher, dass der generierte Code den definierten Architektur-, Stil- und Qualitätsstandards entspricht.
* **Transparenz & Nachvollziehbarkeit:** Jeder Schritt von der Anforderung bis zur Implementierung ist dokumentiert und nachvollziehbar.

---

## **2. Die Dokumente und ihre Synergien**

### **2.1. Project Requirement Details (PRD.md)**

* **Zweck:** Das **PRD** ist die **primäre Quelle** für die Projektdefinition. Es legt fest, *was* gebaut werden soll, und beantwortet Fragen wie „Welches Problem lösen wir?“, „Wer sind unsere Nutzer?“ und „Welche Funktionen benötigt das Projekt?“
* **Beziehung zum System:** Es bildet die Grundlage für die **PTS** (technische Umsetzung), die **PRR** (Planung der Features) und die **PRPs** (konkrete Aufgaben). Die im PRD definierten **User Stories und Akzeptanzkriterien** sind die Endziele, die erreicht werden müssen.

### **2.2. Project Technical Specification (PTS.md)**

* **Zweck:** Die **PTS** beschreibt das *WIE* der technischen Umsetzung. Sie definiert die Systemarchitektur, die wichtigsten Designentscheidungen (ADRs), die Modulstruktur, den Datenfluss und kritische **Coding Standards & Style Guides**.
* **Beziehung zum System:** Sie ergänzt das PRD durch technische Details und stellt sicher, dass der von KI-Agenten generierte Code **konsistent mit der Gesamtarchitektur** und den Qualitätsstandards ist. PRPs werden die Vorgaben aus der PTS integrieren, um präzise, technische Anweisungen zu formulieren.

### **2.3. Project Requirements Roadmap (PRR.md)**

* **Zweck:** Die **PRR** ist ein **dynamisches Planungswerkzeug**, das den Fortschritt verfolgt. Sie listet die Epics/Features aus dem PRD auf, deren Priorität, Status und Abhängigkeiten.
* **Beziehung zum System:** Der **Project- und Technologie-Orchestrator** nutzt die PRR, um den Entwicklungsprozess zu steuern. Sie hilft bei der Entscheidung, welche **PRPs** als Nächstes generiert werden müssen, um die Projektziele effizient zu erreichen, und berücksichtigt dabei technische Abhängigkeiten aus der PTS.

### **2.4. Project Requirement Prompt (PRP.md)**

* **Zweck:** Ein **PRP** ist eine **detaillierte, ausführbare Anweisung** für einen einzelnen, spezialisierten KI-Sub-Agenten (z. B. `Coding-Agent`, `Schema-Agent`, `Test-Agent`). Es übersetzt eine spezifische Anforderung oder einen technischen Task in eine umsetzbare Form.
* **Beziehung zum System:** PRPs sind die **„Arbeitsaufträge“** des Systems. Sie aggregieren Informationen aus dem **PRD** (was zu tun ist) und der **PTS** (wie es technisch umzusetzen ist) und werden vom Project- und Technologie-Orchestrator generiert, basierend auf der **PRR**-Priorisierung.

---

## **3. Anwendung des Systems (Für den Project- und Technologie-Orchestrator)**

Als **Project- und Technologie-Orchestrator** bist du die zentrale Intelligenz, die dieses System steuert. Hier ist der typische Workflow:

1. **Initialisierung:**

   * Beginne mit einem **PRD.md**, das die grundlegenden Projektanforderungen definiert. Passe die Vorlage an euer spezifisches Projekt (z. B. eine Android Habit Tracking App) an.
   * Erstelle eine erste Version der **PTS.md**, die die grundlegende Architektur und die Coding Standards für das Projekt festlegt. Diese wird sich aus den „Technischen Forschungs“-Abschnitten des PRD speisen.
   * Initialisiere die **PRR.md** mit den Haupt-Epics/Features aus dem PRD und setze erste Prioritäten und Schätzungen.

2. **Iterative Entwicklung:**

   * **Priorisierung:** Konsultiere die **PRR**, um die nächsten zu bearbeitenden Epics/Features zu identifizieren. Achte auf Abhängigkeiten.
   * **PRP-Generierung:** Für ein ausgewähltes Feature generiere einen oder mehrere **PRPs**. Ein PRP sollte:

     * Die **Anforderung aus dem PRD** (z. B. eine User Story und deren Akzeptanzkriterien) klar definieren.
     * Die **technischen Vorgaben aus der PTS** integrieren (z. B. welche Architekturmuster zu verwenden sind, welche Datenbank, welche Coding Standards einzuhalten sind).
     * Spezifische Anweisungen für den jeweiligen KI-Sub-Agenten enthalten (z. B. „Coding-Agent: Implementiere die Funktion `createHabit` unter Verwendung des Room-DAOs und folge dem MVVM-Muster.“).
   * **Ausführung durch KI-Agenten:** Die generierten PRPs werden an die spezialisierten KI-Sub-Agenten zur Ausführung weitergegeben.
   * **Feedback & Tests:** Bewerte den Output der KI-Agenten. Führe Tests durch (ggf. durch einen `Test-Agent` via PRP instruiert).
   * **Anpassung & Refinement:** Basierend auf Feedback und Testergebnissen:

     * Passe bei Bedarf das **PRD** an (wenn sich Anforderungen ändern).
     * Aktualisiere die **PTS** (wenn sich architektonische Entscheidungen oder Standards entwickeln).
     * Aktualisiere den Status in der **PRR**.
     * Generiere neue oder korrigierende **PRPs**, um Mängel zu beheben oder nächste Schritte einzuleiten.
   * **Wiederhole diesen Zyklus**, bis alle Anforderungen aus dem PRD erfüllt und die Qualität in der PTS erreicht ist.

3. **Status-Tracking:**

   * Pflege die **PRR** kontinuierlich, um den Überblick über den Fortschritt, offene Punkte und Engpässe zu behalten.
   * Nutze den „Änderungsverlauf“ in PRD, PTS und PRR, um die Evolution der Spezifikationen transparent zu machen.

---

## **4. Repository-Struktur**

```plaintext
/
├── PRD.md            # Project Requirement Details (WAS)
├── PTS.md            # Project Technical Specification (WIE)
├── PRR.md            # Project Requirements Roadmap (STATUS)
├── PRP.md            # Project Requirement Prompt (VORLAGE für AKTIONEN)
└── README.md         # Diese Datei
```

---

Viel Erfolg bei der Nutzung des Systems! Bei Fragen oder zur Weiterentwicklung dieses Frameworks, zögere nicht, Anpassungen vorzunehmen oder Feedback zu geben.
