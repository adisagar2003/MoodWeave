# MoodWeave-Project-Management.md

## Project Manager's Overview
*Hello, I'm the Project Manager assistant for MoodWeave—your efficient sidekick ensuring indie success. Drawing from successful indie devs (e.g., Rob J's 20+ apps: validate ideas via prototypes, ship MVPs fast, market early; Bart Bonte's advice: make small prototypes to de-risk; Unity best practices: test early, focus UX/simplicity), I've structured this as agile sprints for a 1-month MVP. Total: 4 weeks, small team (1-2 devs, 1 designer). Tools: GitHub Projects for tracking, Figma for UX, Slack for comms.

Phases: Planning (Week 0), Sprints (Weeks 1-4), Launch. Assign tasks by role (Dev, Designer, PM). Milestones: Weekly demos. Risks: Scope creep—mitigate with daily standups.*

## Sprint 0: Planning & Research (Pre-Week 1, 2-3 Days)
| Task ID | Description | Assignee | Dependencies | Due Date | Status |
|---------|-------------|----------|--------------|----------|--------|
| PM-001 | Review indie success stories: Summarize key learnings (e.g., "ship 5x faster by scoping 80/20"). Share doc. | PM | None | Day 1 | TODO |
| PM-002 | User validation: Schedule 5-10 interviews (script: pains in journaling/accountability). Log insights. | Designer | PM-001 | Day 2 | TODO |
| DEV-001 | Scaffold repo: Init Expo RN project, add LTS libs (Zustand, Reanimated, etc.). Commit structure. | Dev | None | Day 2 | TODO |
| BACK-001 | Setup Firebase: Create project, init Auth/Firestore/Functions. Define schema. | Dev | None | Day 2 | TODO |
| UX-001 | **UX Start Suggestions**: Kickoff with low-fi wireframes in Figma. Focus: Empathy mapping (user personas: "Solo Struggler"—needs gentle nudges). Tips from research (UX Planet, Biz4Group):<br>- **User-Centered**: Start with journey map (onboard → journal → pair → reflect). Prioritize calm flows (e.g., 3-tap journal entry).<br>- **Glassmorphic Prototypes**: Use Figma's blur effects for mood slider; test color blending (e.g., blue+orange=purple gradient).<br>- **Accessibility**: High contrast for moods; voice-over for entries. Iterate: Share lo-fi with 3 testers for feedback.<br>- **Mindfulness-Specific**: Subtle animations (fade-ins, not jarring); optional dark mode. Benchmark: 5min Journal app—simple prompts reduce overwhelm.<br>Goal: 5 screens prototyped. | Designer | PM-002 | Day 3 | TODO |

## Sprint 1: Core Setup & Onboarding (Week 1)
| Task ID | Description | Assignee | Dependencies | Due Date | Status |
|---------|-------------|----------|--------------|----------|--------|
| DEV-002 | Implement onboarding: Screens for signup, profile, color picker. Integrate Firebase Auth. | Dev | DEV-001 | Day 5 | TODO |
| UX-002 | Design onboarding: Glassmorphic cards; color wheel with preview blend sim. | Designer | UX-001 | Day 4 | TODO |
| BACK-002 | AuthService: Cloud Function for user creation (add color to Firestore). | Dev | BACK-001 | Day 6 | TODO |
| TEST-001 | Unit tests: Auth flows, color utils. | Dev | DEV-002 | Day 7 | TODO |
| PM-003 | Sprint review: Demo onboarding; gather feedback. | All | All Week 1 | Day 7 | TODO |

## Sprint 2: Journaling Core (Week 2)
| Task ID | Description | Assignee | Dependencies | Due Date | Status |
|---------|-------------|----------|--------------|----------|--------|
| DEV-003 | Build journaling: Mood slider (gradient picker), glass input, streak calendar with glow. Private entries to Firestore. | Dev | DEV-002 | Day 10 | TODO |
| UX-003 | Refine journaling UI: Smooth animations; test on device for glow perf. | Designer | UX-002 | Day 9 | TODO |
| BACK-003 | JournalService: Functions for entry CRUD, streak calc. | Dev | BACK-002 | Day 11 | TODO |
| DEV-004 | State: Zustand stores for journal data. | Dev | DEV-003 | Day 12 | TODO |
| TEST-002 | E2E tests: Journal flow. | Dev | DEV-003 | Day 14 | TODO |
| PM-004 | Review: User test journaling (3 betas); adjust based on indie tip: "Simplicity wins retention." | All | All Week 2 | Day 14 | TODO |

## Sprint 3: Pairing & Blending (Week 3)
| Task ID | Description | Assignee | Dependencies | Due Date | Status |
|---------|-------------|----------|--------------|----------|--------|
| DEV-005 | Pairing screens: Invite/random match, shared dashboard with color blend (tinycolor2). | Dev | DEV-004 | Day 17 | TODO |
| UX-004 | Design paired views: Gradient blends, glass panels for progress. | Designer | UX-003 | Day 16 | TODO |
| BACK-004 | PairingService: FIFO matching function; shared notes sync. | Dev | BACK-003 | Day 18 | TODO |
| DEV-006 | Notifications: Expo setup for partner alerts. | Dev | DEV-005 | Day 19 | TODO |
| TEST-003 | Tests: Pairing logic, blend utils. | Dev | DEV-005 | Day 21 | TODO |
| PM-005 | Review: Beta pair test; validate "connected" emotion. | All | All Week 3 | Day 21 | TODO |

## Sprint 4: Polish, Analytics, Launch (Week 4)
| Task ID | Description | Assignee | Dependencies | Due Date | Status |
|---------|-------------|----------|--------------|----------|--------|
| DEV-007 | Analytics: Basic mood chart (Victory); freemium teasers. | Dev | DEV-006 | Day 24 | TODO |
| UX-005 | Final polish: Smooth UX audits; accessibility checks. | Designer | UX-004 | Day 23 | TODO |
| BACK-005 | AnalyticsService: Aggregate functions. Security rules. | Dev | BACK-004 | Day 25 | TODO |
| DEV-008 | Build & submit: Expo EAS for iOS/Android betas. | Dev | DEV-007 | Day 26 | TODO |
| MARK-001 | Prep marketing: ASO keywords, teaser posts on X/Instagram (indie tip: viral invites early). | PM | All | Day 27 | TODO |
| TEST-004 | Full integration tests; perf optimization. | Dev | All | Day 28 | TODO |
| PM-006 | Launch review: Metrics setup (Firebase Analytics); retrospective. | All | All Week 4 | Day 28 | TODO |

## Post-Launch (Ongoing)
- **Iteration Cycle**: Weekly feedback loops (indie best: "Launch, learn, update"). Monitor retention via Firebase.
- **Growth**: Referral bonuses; A/B tests on colors.
- **Escalation**: If blocked >1 day, PM reassigns.

*Project Manager Note: Total effort ~160 hours (scalable for solo). Track in GitHub. Success = Ship & Iterate—celebrate Week 1 milestone with a virtual coffee!*