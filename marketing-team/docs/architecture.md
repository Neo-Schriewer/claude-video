# Architektur (7 Layer, aus dem Diagramm)

| Nr | Layer | Inhalt |
|---|---|---|
| 01 | **Signals** – "where the signal comes from" | Competitor-Rankings, Suchinteresse, Kanal-Analytics, Mentions |
| 02 | **System of Record** – "brand spine, one unified profile" | CRM & Kontakte, Content-Kalender, Asset-Drive, Playbook-Wiki, Segment/CDP, Unified Store, Audience-Liste |
| – | **Owner Input** – *human-led, not counted* | Brand Voice, Budget-Cap, Approval-Bar, Positionierung & Offer |
| 03 | **The Brain** – "the labour" | Claude (Reasoning/Writing), Agent-Runner (LangGraph), Memory-Store (pgvector/Postgres), Midjourney (Visuals), ElevenLabs (Voiceover), Live-Research |
| 03 | **Orchestrator** | Jedes Ereignis kommt zuerst hierher: Collects → Scores → Briefs → Drafts → Schedules → Approves. "Routine content ships end to end. Only budget changes and edge cases reach the owner." Begründet gegen das Playbook, Gedächtnis via pgvector |
| 04 | **Knowledge Layer + Access** | "Marketing OS file system" (ein gemeinsamer Workspace für das ganze Team) + Access Control Plane (Rechte je Agent/Tool) |
| 05 | **Departments** | Sechs Abteilungen, wiederverwendete Tools nur einmal gezählt → `departments.md` |
| 06 | **Engage** | Scheduler, Buffer-artige Queue, Newsletter → erreicht das **Audience** |
| 07 | **Data & Observability** | Dashboards/Analytics/Queries, Feedback in den Loop zurück |

Das Ganze ist ein **Loop**, kein Funnel: Ergebnisse aus Analytics (07) fließen als Signale (01) zurück.

## Abbildung hier
- Orchestrator + Departments → `.claude/agents/`
- Knowledge Layer → `marketing-os/`
- System of Record / Brain / Engage → externe Tools (siehe `tool-stack.md`); anfangs durch Dateien in `marketing-os/` ersetzbar
- Access Control → in Claude Code über `tools:` je Agent (Frontmatter) und Permission-Settings
