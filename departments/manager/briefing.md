# Manager Briefing System

Persistent memory for cross-session continuity. Every project gets a briefing. Every session starts with reading it.

**CRITICAL: Briefings are PER-PROJECT, not global. Each project has its own `.manager-briefing.md` in its root directory.**

---

## How It Works

1. **Per-Project Storage**: Each project has its own `.manager-briefing.md` in its root directory
   - Example: `C:\Users\TechTroniX\teller\.manager-briefing.md`
   - Example: `C:\Users\TechTroniX\my-app\.manager-briefing.md`
   - NOT in home directory or a central location
2. **On Session Start**: Manager checks current working directory, then reads that project's briefing
3. **On Session End**: Manager updates that project's briefing with progress
4. **On Major Milestones**: Manager updates the briefing immediately
5. **Project Isolation**: Each project's context is completely separate

---

## Briefing Document Template

When creating a briefing for a project, use this exact structure:

```markdown
# Project Briefing: [PROJECT_NAME]

**Last Updated**: [DATE]
**Session Count**: [NUMBER]
**Overall Status**: [NOT_STARTED | IN_PROGRESS | BLOCKED | REVIEW | COMPLETE]

---

## 1. Project Overview

### What We're Building
[1-3 sentence description of the project]

### Why It Matters
[Business context - who is this for, what problem does it solve]

### Success Criteria
[What does "done" look like - measurable outcomes]

---

## 2. OKRs

**Objective**: [The goal we're trying to achieve]

**Key Results**:
1. [ ] [Measurable result 1]
2. [ ] [Measurable result 2]
3. [ ] [Measurable result 3]

---

## 3. Current Status

### Phase
[DISCOVERY | STRATEGY | DESIGN | BUILD | INTEGRATION | LAUNCH]

### Progress Summary
[2-3 sentences on where we are right now]

### Completed
- [x] [Thing that's done]
- [x] [Thing that's done]

### In Progress
- [ ] [Current work item]

### Blocked
- [Blocker description and what's needed to unblock]

---

## 4. Key Decisions

Decisions made that future sessions need to know:

| Decision | Rationale | Date |
|----------|-----------|------|
| [What was decided] | [Why] | [When] |

---

## 5. Domain Context

### Business (Hormozi)
- **Target Audience**: [Who]
- **Value Proposition**: [What]
- **Pricing/Offer**: [How monetized]
- **Key Constraints**: [Limits]

### Design
- **Design System**: [Colors, fonts, spacing if established]
- **Key Screens**: [List of main screens/flows]
- **Mobile Strategy**: [Mobile-first? Responsive? Native?]
- **Accessibility**: [Requirements]

### Code (Developer-Hat)
- **Tech Stack**: [Languages, frameworks, tools]
- **Architecture**: [Key patterns, structure]
- **Key Files**: [Critical files to know about]
- **Dependencies**: [External services, APIs]

---

## 6. Open Questions

Questions that need answers before proceeding:

1. [Question 1]
2. [Question 2]

---

## 7. Next Actions

Priority-ordered list of what to do next:

1. **[HIGH]** [Action item]
2. **[MEDIUM]** [Action item]
3. **[LOW]** [Action item]

---

## 8. Session Log

### Session [N] - [DATE]
**Focus**: [What we worked on]
**Accomplished**: [What got done]
**Blockers Hit**: [Any issues]
**Next Session**: [What to do next time]

---

## 9. Quality Scores (Last Review)

| Domain | Score | Notes |
|--------|-------|-------|
| Requirements | /10 | |
| Design | /10 | |
| Business | /10 | |
| Code | /10 | |
| Integration | /10 | |
| **OVERALL** | /10 | |

---

## 10. Red Flags

Critical issues that must be addressed:

- [Red flag 1]
- [Red flag 2]
```

---

## Manager Startup Protocol

When `/manager` is invoked, IMMEDIATELY:

1. **Check working directory**: Determine if in a project directory or home/generic directory
2. **If in home/generic directory**: Ask user to navigate to project or specify path
3. **If in project directory**: Look for `.manager-briefing.md` in that project's root
4. **If briefing exists**: Read it completely before responding
5. **If no briefing in project**: Ask user if this is a new or existing project
   - New project: Create briefing template in project root
   - Existing project: Ask for context to populate briefing

### If in Home/Generic Directory - Response Format:

```
## No Project Context

I need to be in a project directory to manage work effectively.

Options:
1. **Navigate to project** - `cd your-project-name` then invoke me again
2. **Tell me the project path** - I'll check for its briefing
3. **One-off task** - No project context needed

Which is it?
```

### When a briefing exists in project:

```
## Resuming: [PROJECT_NAME]

**Status**: [STATUS] | **Phase**: [PHASE] | **Sessions**: [N]

### Where We Left Off
[Summary from last session log]

### Today's Priority
[First item from Next Actions]

### Blockers
[Any blockers from briefing]

Ready to continue. What's the focus today?
```

### When in project but no briefing exists:

```
## No Project Briefing Found in [DIRECTORY_NAME]

Is this:
1. **New project** - I'll create `.manager-briefing.md` here to track our work
2. **Existing project** - Give me context and I'll document it
3. **One-off task** - No briefing needed

Which is it?
```

---

## Briefing Update Triggers

Update the briefing when:

1. **Session ends** - User says goodbye, done, etc.
2. **Major decision made** - Add to Key Decisions
3. **Phase changes** - Update Current Status
4. **Blocker encountered** - Add to Blocked section
5. **Blocker resolved** - Move from Blocked to Completed
6. **Quality review done** - Update Quality Scores
7. **Red flag identified** - Add to Red Flags

### Update Protocol

When updating:
1. Read current briefing
2. Make targeted changes (don't rewrite everything)
3. Update "Last Updated" timestamp
4. Increment session count if new session
5. Add to Session Log

---

## Commands

Users can trigger briefing actions:

| Command | Action |
|---------|--------|
| `briefing:create` | Create new briefing for current project |
| `briefing:read` | Display current briefing |
| `briefing:update` | Update briefing with current status |
| `briefing:status` | Show quick status summary |
| `briefing:log` | Add entry to session log |
| `briefing:decision` | Log a key decision |
| `briefing:blocker` | Add a blocker |
| `briefing:resolve` | Mark blocker as resolved |

---

## Example Briefing

```markdown
# Project Briefing: Teller App

**Last Updated**: 2026-01-04
**Session Count**: 3
**Overall Status**: IN_PROGRESS

---

## 1. Project Overview

### What We're Building
A personal finance app for Muslim users with halal investment tracking, zakat calculations, and spending insights.

### Why It Matters
Muslim users need finance tools that respect Islamic principles. Existing apps don't handle halal screening or zakat properly.

### Success Criteria
- Users can track halal vs non-halal investments
- Automatic zakat calculations at year end
- Clean, intuitive expense tracking

---

## 2. OKRs

**Objective**: Launch MVP with core finance tracking and Islamic finance features

**Key Results**:
1. [ ] Transaction import and categorization working
2. [x] Halal stock screening integrated
3. [ ] Zakat calculator complete
4. [ ] User testing with 5 target users

---

## 3. Current Status

### Phase
BUILD

### Progress Summary
Core transaction tracking is complete. Working on zakat calculator. Halal screening API integrated but needs UI polish.

### Completed
- [x] Supabase authentication
- [x] Transaction CRUD
- [x] Basic spending categories
- [x] Halal screening API integration

### In Progress
- [ ] Zakat calculator logic
- [ ] Investment portfolio screen

### Blocked
- None currently

---

## 4. Key Decisions

| Decision | Rationale | Date |
|----------|-----------|------|
| React Native + Expo | Cross-platform, fast iteration | 2026-01-02 |
| Supabase for backend | Auth + DB + realtime, no server management | 2026-01-02 |
| Manual categorization first | Auto-categorization too complex for MVP | 2026-01-03 |

---

## 5. Domain Context

### Business (Hormozi)
- **Target Audience**: Muslim professionals 25-45 managing investments
- **Value Proposition**: Only finance app that handles zakat and halal screening
- **Pricing/Offer**: Free basic, $9.99/mo premium with full halal screening
- **Key Constraints**: Must be Sharia-compliant, no interest-based features

### Design
- **Design System**: Green/gold palette, Inter font, 8px spacing grid
- **Key Screens**: Dashboard, Transactions, Investments, Zakat, Settings
- **Mobile Strategy**: Mobile-first, React Native
- **Accessibility**: Min AA contrast, 44pt touch targets

### Code (Developer-Hat)
- **Tech Stack**: React Native, Expo, TypeScript, Supabase, Zustand
- **Architecture**: Feature-based folders, custom hooks for data
- **Key Files**: `src/features/`, `src/hooks/useTransactions.ts`
- **Dependencies**: Supabase, Musaffa API (halal screening)

---

## 6. Open Questions

1. How to handle partial halal compliance (e.g., 95% halal portfolio)?
2. Should zakat reminder be push notification or in-app only?

---

## 7. Next Actions

1. **[HIGH]** Complete zakat calculator business logic
2. **[HIGH]** Build investment portfolio UI
3. **[MEDIUM]** Add transaction filtering/search
4. **[LOW]** Settings screen

---

## 8. Session Log

### Session 3 - 2026-01-04
**Focus**: Zakat calculator
**Accomplished**: Defined zakat rules, started calculator component
**Blockers Hit**: None
**Next Session**: Complete calculator, connect to portfolio data

### Session 2 - 2026-01-03
**Focus**: Halal screening integration
**Accomplished**: Musaffa API connected, basic stock lookup working
**Blockers Hit**: API rate limits - need caching
**Next Session**: Add caching layer, build zakat calculator

### Session 1 - 2026-01-02
**Focus**: Project setup and architecture
**Accomplished**: Expo project created, Supabase configured, auth working
**Blockers Hit**: None
**Next Session**: Build transaction tracking

---

## 9. Quality Scores (Last Review)

| Domain | Score | Notes |
|--------|-------|-------|
| Requirements | 7/10 | Core features defined, need user validation |
| Design | 6/10 | Basic screens done, needs polish |
| Business | 8/10 | Clear value prop and monetization |
| Code | 8/10 | Clean architecture, good patterns |
| Integration | 7/10 | Parts working, not fully connected |
| **OVERALL** | 7/10 | Solid MVP progress, needs design polish |

---

## 10. Red Flags

- Design system not fully documented - risk of inconsistency
- No automated tests yet - will slow down later
```

---

## Integration with Manager Skill

The briefing system is core to Manager operations:

1. **Before any work**: Read briefing
2. **During work**: Reference OKRs and decisions
3. **After milestones**: Update briefing
4. **End of session**: Log session and next steps

The briefing IS the manager's memory. Treat it as sacred. Keep it accurate. Keep it updated.

**If briefing is stale, the manager is blind.**
