---
trigger: always_on
---

Before declaring anything complete, validate it against these acceptance criteria:

Gameplay:
- A full game can be played from room creation to final scoring.
- The game supports 5 to 8 players.
- The game contains 3 distinct rounds.
- Each round includes briefing, private update, action, private contact, assembly, and resolution phases.
- Players receive hidden roles, goals, and ultimates.
- Scoring includes team points, personal goal points, and insight points.

Multiplayer:
- A host can create a room.
- Other players can join via room code or link.
- Player presence is synchronized.
- Phase changes are synchronized.
- Submitted actions are synchronized and locked correctly.
- Public decisions are synchronized.
- Late joins after game start are handled safely.
- Reconnect behavior fails gracefully.

UI/UX:
- The game is attractive and polished on desktop and mobile.
- The UI clearly separates public information and private information.
- Timers are readable.
- Actions and phases are understandable without reading large walls of text.
- Role cards, zone panels, logs, and scoreboards are visually distinct.

Technical:
- Uses Next.js + TypeScript + Supabase Realtime.
- Has a clean file structure.
- Has .env.example.
- Includes setup and deployment steps.
- Can be deployed to Vercel.
- No critical hardcoded secrets.
- No broken local-only assumptions.

Content:
- Includes 3 full incident rounds.
- Includes a reusable role pool.
- Includes at least 20 personal goals.
- Includes a meaningful ultimate pool.
- Content is data-driven, not scattered across random components.

Failure states:
- Empty lobby handled.
- Not enough players handled.
- Disconnected player handled.
- Timer expiry handled.
- Missing action submission handled.
- Invalid room handled.
- Duplicate nickname collision handled.