# School OS

Dasselbe Prinzip wie das "One-Person Marketing Team" (Orchestrator + Spezialisten + gemeinsamer Dateispeicher), aber fürs Lernen. Alles gratis.

## Grundprinzip (wichtig)
Die KI ist **Tutor und Feedback-Geber, nicht Ghostwriter.** Gründe:
1. Wer Hausaufgaben abschreibt, lernt nichts, und in Klausuren hast du keine KI.
2. Viele Schulen werten KI-Texte ohne Kennzeichnung als Täuschungsversuch. Lehrer erkennen den "KI-Stil" oft.
3. Gute Noten kommen durch Verständnis + sauber erfüllte Bewertungskriterien. Dabei hilft das System.

## Benutzen
```bash
cd school-os && claude
```
Beispiele: `Plane meine Woche`, `Erkläre mir <Thema> und frag mich dann ab`, `Gib Feedback zu meinem Aufsatz in tasks/aufsatz.md`, `Mach aus meinen Notizen Karteikarten`.

## Zuerst ausfüllen (10 Min)
`profile/school.md`, `profile/goals.md`, `profile/integrity-rules.md`, `profile/time-budget.md`.

## Struktur
| Pfad | Zweck |
|---|---|
| `CLAUDE.md` | Regeln des Orchestrators |
| `.claude/agents/` | Orchestrator + 5 Spezialisten |
| `profile/` | Deine Vorgaben (statt Brand/Budget) |
| `subjects/` | Pro Fach: Themen, Bewertungskriterien, Termine |
| `tasks/` | Aufgaben, Abgaben, Entwürfe von dir |
| `notes/` | Zusammenfassungen und Erklärungen |
| `flashcards/` | Karteikarten (Anki-importierbar, CSV) |
| `feedback/` | Rückmeldungen und Fehlerlog |
| `docs/free-tools.md` | Gratis-Tools |
