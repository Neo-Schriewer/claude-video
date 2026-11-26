# The One-Person Marketing Team

> **Zweck hier: Athleten-Marke von Neo (Basketball).** Siehe `docs/athlete-brand.md` und `marketing-os/brand/safety-rules.md`.

Nachbau der Architektur aus dem TikTok von **@structurewebworks** ("The One-Person Marketing Team", 36 Agenten).
Ziel: Ein Mensch (Owner) gibt Rahmen vor, ein Orchestrator mit sechs Abteilungen erledigt den Rest.

## Wichtig: Herkunft und Grenzen
- Quelle ist **nur das Diagramm im Video** (ohne Transkript, Tonspur nicht auswertbar). Layer, Abteilungen, Tool-Namen und "Interrupts" sind abgelesen. Tool-Namen mit `(vermutet)` sind aus Icons abgeleitet.
- Die Datei-Struktur des "Marketing OS" war im Video unleserlich klein. `marketing-os/` ist **meine Rekonstruktion**, nicht das Original.
- Das Video verweist für den Deep-Dive auf den Blog `structurewebworks.com/blog`. Dort liegt vermutlich das Original-Breakdown.
- Die "36 Agenten" sind eine Marketingzahl. Hier sind es 1 Orchestrator + 6 Abteilungs-Agenten (`.claude/agents/`), die du beliebig weiter aufteilen kannst.

## Benutzen
```bash
cd marketing-team
claude            # Claude Code liest CLAUDE.md + .claude/agents/
```
Dann z. B.: `Starte einen Loop-Durchlauf für diese Woche` oder `Trend-Spike: <Thema>, reagiere nach loop-interrupts.md`.

**Zuerst ausfüllen (Owner Input, ca. 30 Min):** `marketing-os/brand/` (Voice, Positionierung & Offer, Budget-Cap, Approval-Bar). Ohne das produziert das System generischen Output.

## Inhalt
| Pfad | Zweck |
|---|---|
| `CLAUDE.md` | Orchestrator-Regeln (Collect → Score → Brief → Draft → Schedule → Approve) |
| `.claude/agents/` | Orchestrator + 6 Abteilungen als Subagenten |
| `marketing-os/` | Wissensschicht (gemeinsamer Dateispeicher aller Agenten) |
| `docs/architecture.md` | 7 Layer des Diagramms |
| `docs/departments.md` | Abteilungen mit Tools |
| `docs/loop-interrupts.md` | Ereignisse, die den Loop auslösen |
| `docs/tool-stack.md` | Tool-Liste, Kosten-/Ersatz-Hinweise |
| `docs/reference/` | Screenshots aus dem Video |

## Kritische Einschätzung
- Vollautomatisches Veröffentlichen ohne Freigabe ist riskant (Markenschaden, Plattform-Sperren, Halluzinationen). Standard hier: **nichts geht live ohne Approval**, bis du `approval-bar.md` bewusst lockerst.
- Das Original-Setup umfasst ~30 Tools. Für den Start reichen: Claude, ein Scheduler (Buffer), ein Newsletter-Tool, GA4. Rest erst bei nachgewiesenem Engpass.
