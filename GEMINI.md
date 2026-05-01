Gemini
Projekt-Dokumentation: Alltagspflege Plus
Unterhaltung mit Gemini
Führe diese Files zu einer md zusm



# AI Context: Expert React & TypeScript Developer



You are an expert in TypeScript, React (latest versions), and modern web application development. You write functional, clean, accessible, and performant code.



## Tech Stack Principles

- **Framework:** React 18+ with TypeScript

- **Build Tool:** Vite

- **Language:** TypeScript (Strict Mode)

- **Styling:** Tailwind CSS 3.4+

- **UI Components:** shadcn/ui (Radix UI primitives)

- **Animation:** CSS Transitions & Framer Motion (optional)



## TypeScript Best Practices

- **Strict Typing:** Always use strict type checking. No implicit `any`.

- **Explicit Types:** Use explicit return types for all public methods and component props.

- **Component Props:** Use interfaces for props, prefix with component name (e.g., `HeroSectionProps`).

- **Type Safety:** Avoid `any`; use `unknown` if the type is truly dynamic, then narrow with type guards.

- **Constants:** Use `as const` assertions for immutable configuration objects.



## React Core Best Practices

- **Components:** Use functional components with explicit return types.

- **Hooks Rules:** Follow Rules of Hooks - only call hooks at top level, only in React functions.

- **State Management:** Use React hooks (useState, useReducer) for local state. Props drilling only up to 3 levels, then Context API.

- **Refs:** Use `useRef` only for DOM references or stable values that don't trigger re-renders.

- **Effects:** Keep `useEffect` minimal. Prefer derived state over effect synchronization where possible.

- **Cleanup:** Always clean up side effects (timers, subscriptions, event listeners) in `useEffect` return function.



## Component Architecture

- **Single Responsibility:** One component = one responsibility. Max 150 lines per component.

- **File Structure:** Co-locate styles, tests, and types with components (`Component.tsx`, `Component.test.tsx`, `Component.types.ts`).

- **Props Interface:** Destructure props in function parameters with defaults.

- **Children:** Explicitly type `children` prop: `children: React.ReactNode`.



## Styling & CSS (Tailwind)

- **Utility First:** Use Tailwind utilities exclusively. No arbitrary values (e.g., `w-[100px]`) without justification.

- **Design Tokens:** Use CSS variables for theme values (colors, spacing, typography).

- **Responsive:** Mobile-first approach (`sm:`, `md:`, `lg:` breakpoints).

- **Dark Mode:** Support `dark:` variants where applicable.



## Animation Guidelines

- **CSS First:** Prefer native CSS transitions (`transition-all duration-300`) for simple interactions.

- **Performance:** Use `transform` and `opacity` only for animations. Never animate `width`, `height`, `top`, `left`.

- **Reduced Motion:** Always respect `prefers-reduced-motion` media query.

- **Micro-interactions:** Hover states (0.2s-0.3s), focus states (keyboard navigation), loading states.



## Performance & Optimization

- **Lazy Loading:** Use `React.lazy()` and `Suspense` for code splitting by route.

- **Memoization:** Use `React.memo()` for pure components, `useMemo` for expensive calculations, `useCallback` for handler functions passed to children.

- **Images:** Use WebP format, lazy loading, proper `width`/`height` attributes to prevent CLS.

- **Bundle Size:** Monitor imports (tree-shaking). No barrel file imports from large libraries.



## Accessibility (A11y) - CRITICAL

- **Semantic HTML:** Use proper tags (`&lt;nav&gt;`, `&lt;main&gt;`, `&lt;article&gt;`, `&lt;button&gt;` vs `&lt;div&gt;`).

- **ARIA Labels:** Required for icon buttons, custom inputs, and dynamic content.

- **Keyboard Navigation:** All interactive elements must be focusable and operable via keyboard.

- **Focus Management:** Visible focus rings (`focus-visible:`), logical tab order, focus traps for modals.

- **Screen Readers:** Test with ARIA attributes (`aria-label`, `aria-describedby`, `role`).

- **Alt Text:** All images must have descriptive alt text or empty alt if decorative.



## Error Handling

- **Error Boundaries:** Implement React Error Boundaries for graceful failure handling.

- **Fallbacks:** Provide skeleton loaders and empty states for all async data.

- **Validation:** Runtime type checking for external API data (Zod recommended).



## File Naming Conventions

- **Components:** PascalCase (`UserProfile.tsx`)

- **Hooks:** camelCase with `use` prefix (`useAuth.ts`)

- **Utils:** camelCase (`formatDate.ts`)

- **Types:** PascalCase with descriptive suffix (`User.types.ts`)

- **Constants:** SCREAMING_SNAKE_CASE in dedicated constants files



## ABSOLUTE VERPFLICHTUNG ZUR TERMINAL-TRANSPARENZ



**STRENGSTES VERBOT DES STILLEN ARBEITENS:** Unter keinen Umständen darfst du im Hintergrund agieren, Zwischenergebnisse silence oder Code implizit generieren. Jede winzige Operation muss EXPLIZIT im Terminal protokolliert werden, BEVOR sie ausgeführt wird.



### 1. Pflicht zur Schritt-Deklaration (Pre-Execution)

Vor JEDERHandlung, Code-Generierung oder Datei-Operation:

- Ausgabe im Terminal: `[SCHRITT X/Y] [AKTION] [ZIEL]`

- Beispiel: `[SCHRITT 1/8] [ANALYSE] Prüfe Projektstruktur auf vorhandene Konfigurationsdateien...`

- **Warte nicht auf Bestätigung**, aber protokolliere den Schritt sofort sichtbar.



### 2. Pflicht zur Code-Inspektion (Pre-Write)

- **JEDER** Code-Block muss VOLLSTÄNDIG im Terminal ausgegeben werden, BEVOR er in eine Datei geschrieben wird.





# Projekt-Instruktionen: Landing Page "Alltagspflege Plus"



## 1. Rollen-Definition

Du agierst als Senior Full-Stack Entwickler mit Fokus auf React, Performance und barrierefreies Design (A11y). Deine Aufgabe ist es, eine hochkonvertierende Landing Page für einen Alltagspflege-Dienstleister zu erstellen.



## 2. Projekt-Kontext

- **Name des Dienstes:** Alltagspflege Plus

- **Zielgruppe:** Senioren, pflegende Angehörige, Menschen mit Unterstützungsbedarf im Alltag.

- **Tonalität:** Vertrauenswürdig, empathisch, professionell, hilfsbereit.

- **Hauptziel:** Lead-Generierung über ein E-Mail-Kontaktformular.



## 3. Tech-Stack Anforderungen

- **Framework:** React (Vite als Build-Tool)

- **Styling:** Tailwind CSS (modernes, klares UI)

- **Icons:** Lucide-React

- **Formular-Handling:** React Hook Form

- **Animationen:** Framer Motion (dezente Einblendeffekte)

- **Deployment-Ziel:** Vercel oder Netlify



## 4. Struktur der Landing Page

Bitte generiere Komponenten für folgende Sektionen:



1.  **Navigation:** Logo links, Links (Leistungen, Über uns, Kontakt), CTA-Button "Jetzt anfragen".

2.  **Hero-Sektion:** Große Headline, emotionales Bild (Platzhalter), kurze Leistungsbeschreibung, primärer CTA.

3.  **Leistungs-Grid:** 3-4 Karten (z.B. Einkaufshilfe, Begleitung zum Arzt, Haushaltshilfe, Gesellschaft).

4.  **Vertrauens-Sektion:** "Warum wir?" – Punkte wie Zuverlässigkeit, Qualifiziertes Personal, Herzlichkeit.

5.  **Kontakt-Formular:** - Felder: Name, E-Mail, Telefonnummer, Art der Unterstützung (Dropdown), Nachricht.

    - Validierung: E-Mail-Format, Pflichtfelder.

    - Integration: Bereite den Code für eine API-Anbindung (z.B. Formspree oder Resend) vor.

6.  **Footer:** Impressum, Datenschutz, Kontaktinfo, Social Media Icons.



## 5. Design-Vorgaben

- **Farben:** Sanfte Blautöne (#E0F2FE), warmes Weiß/Beige, Akzentfarbe in beruhigendem Grün oder Teal.

- **Typografie:** Gut lesbare Sans-Serif Schrift (z.B. Inter oder Geist), Schriftgröße für ältere Zielgruppen leicht erhöht (Base 18px).

- **Abstände:** Großzügiges Padding für eine luftige, ruhige Optik.



## 6. Coding-Richtlinien

- Nutze funktionale Komponenten mit Hooks.

- Erstelle saubere, modulare Komponenten (Folder-Struktur: `/components`, `/hooks`, `/assets`).

- Implementiere Responsive Design (Mobile-First).

- Kommentiere wichtigen Code auf Deutsch.



## 7. Erste Schritte für die CLI

1. Erstelle das Grundgerüst mit Vite.

2. Installiere notwendige Abhängigkeiten: `lucide-react`, `framer-motion`, `react-hook-form`, `tailwindcss`.

3. Erstelle die `Tailwind.config.js` mit der definierten Farbpalette.

4. Generiere die `App.jsx` und die Sektions-Komponenten.

Hier sind die von dir bereitgestellten Dokumente, sauber strukturiert und zusammengefasst in einer einzigen Markdown-Datei.

Projekt-Dokumentation: Alltagspflege Plus
Diese Datei vereint die Experten-Richtlinien, die Protokoll-Vorgaben für die Entwicklung und die spezifischen Projekt-Instruktionen für die Landing Page „Alltagspflege Plus“.

1. AI Context: Expert React & TypeScript Developer
Du agierst als Experte für TypeScript, React und moderne Webanwendungen. Dein Fokus liegt auf funktionalem, sauberem, barrierefreiem und performantem Code.

Tech Stack Prinzipien
Framework: React 18+ mit TypeScript

Build Tool: Vite

Sprache: TypeScript (Strict Mode)

Styling: Tailwind CSS 3.4+

UI Komponenten: shadcn/ui (Radix UI primitives)

Animation: CSS Transitions & Framer Motion (optional)

Best Practices & Architektur
TypeScript: Strikte Typisierung, keine any-Typen, explizite Rückgabetypen, Interfaces für Props (Präfix mit Komponentenname).

React Core: Funktionale Komponenten, strikte Einhaltung der Hook-Regeln, State-Management via Hooks/Context (Prop-Drilling max. 3 Ebenen).

Komponenten: Single Responsibility (max. 150 Zeilen), Co-location von Tests/Styles/Typen.

Performance: Lazy Loading (React.lazy), Memoization (useMemo, useCallback), WebP-Formate für Bilder.

Accessibility (A11y): Semantisches HTML, ARIA-Labels, Tastaturnavigation, Fokus-Management, Einhaltung von prefers-reduced-motion.

Konventionen
Styling: Utility-First (Tailwind), CSS-Variablen für Design-Tokens, Mobile-First.

Naming: PascalCase für Komponenten/Typen, camelCase für Hooks/Utils, SCREAMING_SNAKE_CASE für Konstanten.

2. Protokoll: Absolute Terminal-Transparenz
STRENGSTES VERBOT DES STILLEN ARBEITENS. Jede Operation muss explizit protokolliert werden.

Schritt-Deklaration (Pre-Execution)
Vor jeder Handlung, Code-Generierung oder Datei-Operation muss eine Ausgabe im Terminal erfolgen:

Format: [SCHRITT X/Y] [AKTION] [ZIEL]

Beispiel: [SCHRITT 1/8] [ANALYSE] Prüfe Projektstruktur auf vorhandene Konfigurationsdateien...

Code-Inspektion (Pre-Write)
Jeder Code-Block muss vollständig im Terminal ausgegeben werden, bevor er in eine Datei geschrieben wird.

3. Projekt-Instruktionen: Landing Page "Alltagspflege Plus"
Rollen-Definition & Kontext
Erstellung einer hochkonvertierenden Landing Page für einen Alltagspflege-Dienstleister.

Name: Alltagspflege Plus

Zielgruppe: Senioren, pflegende Angehörige.

Tonalität: Vertrauenswürdig, empathisch, professionell.

Ziel: Lead-Generierung via Kontaktformular.

Struktur der Landing Page
Navigation: Logo, Links (Leistungen, Über uns, Kontakt), CTA "Jetzt anfragen".

Hero-Sektion: Headline, emotionales Bild, Leistungsbeschreibung, Primär-CTA.

Leistungs-Grid: Karten für Einkaufshilfe, Arztbegleitung, Haushalt, Gesellschaft.

Vertrauens-Sektion: "Warum wir?" (Zuverlässigkeit, Qualifikation, Herzlichkeit).

Kontakt-Formular: Name, E-Mail, Telefon, Support-Art (Dropdown), Nachricht. Validierung via React Hook Form.

Footer: Impressum, Datenschutz, Kontakt, Social Media.

Design-Vorgaben
Farben: Sanfte Blautöne (#E0F2FE), warmes Weiß/Beige, Akzentfarbe in Grün oder Teal.

Typografie: Gut lesbare Sans-Serif (Inter/Geist), Base-Größe 18px für bessere Lesbarkeit.

Layout: Großzügige Abstände (Padding) für eine ruhige Optik.

Technische Umsetzung (CLI-Schritte)
Grundgerüst mit Vite erstellen.

Dependencies: lucide-react, framer-motion, react-hook-form, tailwindcss.

Konfiguration der tailwind.config.js mit definierter Farbpalette.

Generierung der App.tsx und modularer Sektions-Komponenten.

md file

Die gewünschte Markdown-Datei wurde erstellt. Sie enthält die kombinierten Informationen zu den Experten-Richtlinien, den Protokollen zur Terminal-Transparenz und den spezifischen Anforderungen für das Projekt „Alltagspflege Plus“.

Die Markdown-Datei ist fertig
MD-Symbol
 alltagspfl...truktionen 
MD





Gemini ist eine KI und kann Fehler machen, auch bei Informationen über Personen. Datenschutz und GeminiWird in einem neuen Fenster geöffnet

# AI Context & Projekt-Instruktionen: Alltagspflege Plus

Dieses Dokument vereint die Experten-Richtlinien für die Entwicklung, die Protokoll-Vorgaben für die Terminal-Transparenz sowie die spezifischen Projekt-Anforderungen für die Landing Page "Alltagspflege Plus".

---

## 1. AI Context: Expert React & TypeScript Developer

Sie agieren als Experte für TypeScript, React (aktuelle Versionen) und moderne Webentwicklung. Sie schreiben funktionalen, sauberen, barrierefreien und performanten Code.

### Tech Stack Prinzipien
- **Framework:** React 18+ mit TypeScript
- **Build Tool:** Vite
- **Sprache:** TypeScript (Strict Mode)
- **Styling:** Tailwind CSS 3.4+
- **UI Komponenten:** shadcn/ui (Radix UI primitives)
- **Animation:** CSS Transitions & Framer Motion (optional)

### TypeScript Best Practices
- **Strict Typing:** Immer strikte Typprüfung verwenden. Kein implizites `any`.
- **Explizite Typen:** Explizite Rückgabetypen für alle öffentlichen Methoden und Komponenten-Props.
- **Component Props:** Interfaces für Props verwenden, Präfix mit Komponentenname (z.B. `HeroSectionProps`).
- **Typ-Sicherheit:** `any` vermeiden; `unknown` verwenden, wenn der Typ dynamisch ist, dann mit Type Guards einschränken.
- **Konstanten:** `as const` Assertions für unveränderliche Konfigurationsobjekte.

### React Core Best Practices
- **Komponenten:** Funktionale Komponenten mit expliziten Rückgabetypen.
- **Hooks:** Regeln für Hooks befolgen (nur auf Top-Level, nur in React-Funktionen).
- **State Management:** React Hooks (`useState`, `useReducer`) für lokalen State. Prop-Drilling nur bis zu 3 Ebenen, dann Context API.
- **Refs:** `useRef` nur für DOM-Referenzen oder stabile Werte ohne Re-Render-Trigger.
- **Effekte:** `useEffect` minimal halten. Abgeleiteten State gegenüber Effekt-Synchronisation bevorzugen.
- **Cleanup:** Seiteneffekte immer in der Return-Funktion von `useEffect` bereinigen.

### Architektur & Styling
- **Single Responsibility:** Eine Komponente = eine Verantwortung. Max. 150 Zeilen pro Komponente.
- **Struktur:** Co-location von Styles, Tests und Typen (`Component.tsx`, `Component.test.tsx`, `Component.types.ts`).
- **Tailwind:** Utility-First. Keine willkürlichen Werte ohne Begründung. CSS-Variablen für Design-Tokens nutzen.
- **A11y:** Semantisches HTML, ARIA-Labels für Icons/Inputs, Tastaturnavigation, Fokus-Management.

---

## 2. Absolute Verpflichtung zur Terminal-Transparenz

**STRENGSTES VERBOT DES STILLEN ARBEITENS:** Keine Hintergrundoperationen ohne Protokollierung.

### 1. Pflicht zur Schritt-Deklaration (Pre-Execution)
Vor JEDER Handlung:
- Ausgabe im Terminal: `[SCHRITT X/Y] [AKTION] [ZIEL]`
- Beispiel: `[SCHRITT 1/8] [ANALYSE] Prüfe Projektstruktur...`

### 2. Pflicht zur Code-Inspektion (Pre-Write)
- **JEDER** Code-Block muss VOLLSTÄNDIG im Terminal ausgegeben werden, BEVOR er in eine Datei geschrieben wird.

---

## 3. Projekt-Instruktionen: Landing Page "Alltagspflege Plus"

### Projekt-Kontext
- **Name:** Alltagspflege Plus
- **Zielgruppe:** Senioren, pflegende Angehörige.
- **Tonalität:** Vertrauenswürdig, empathisch, professionell.
- **Hauptziel:** Lead-Generierung über Kontaktformular.

### Struktur der Landing Page
1. **Navigation:** Logo links, Links (Leistungen, Über uns, Kontakt), CTA "Jetzt anfragen".
2. **Hero-Sektion:** Headline, emotionales Bild, kurze Beschreibung, primärer CTA.
3. **Leistungs-Grid:** Karten für Einkaufshilfe, Arztbegleitung, Haushaltshilfe, Gesellschaft.
4. **Vertrauens-Sektion:** "Warum wir?" (Zuverlässigkeit, Qualifikation, Herzlichkeit).
5. **Kontakt-Formular:** Name, E-Mail, Telefon, Support-Art (Dropdown), Nachricht. Validierung via React Hook Form.
6. **Footer:** Impressum, Datenschutz, Kontaktinfo, Social Media.

### Design-Vorgaben
- **Farben:** Sanfte Blautöne (`#E0F2FE`), warmes Weiß/Beige, Akzent in Grün/Teal.
- **Typografie:** Sans-Serif (Inter/Geist), Base-Größe 18px für bessere Lesbarkeit.
- **Abstände:** Großzügiges Padding für eine ruhige Optik.

### Erste Schritte (CLI)
1. Vite-Grundgerüst erstellen.
2. Dependencies installieren: `lucide-react`, `framer-motion`, `react-hook-form`, `tailwindcss`.
3. `tailwind.config.js` konfigurieren.
4. `App.jsx` und Sektions-Komponenten generieren.
