# THEBOLDS Team Systems

**How we operate. How we win.**

---

## 1. STANDARD OPERATING PROCEDURES (SOPs)

### SOP-001: New Project Kickoff

**Trigger:** Mohammad or m7zm initiates a new project

**Steps:**
1. m7zm receives brief and classifies project type
2. m7zm identifies required departments (minimum 2, maximum all)
3. Faisal runs 30-minute research sprint on domain
4. Hormozi validates business case (is this worth building?)
5. All involved departments get briefed simultaneously
6. Each department states:
   - What they need to start
   - What they'll deliver
   - Blockers they foresee
7. m7zm creates project briefing (`.manager-briefing.md`)
8. Saud sets team accountability targets

**Output:** Aligned team, clear deliverables, documented plan

---

### SOP-002: Feature Request

**Trigger:** New feature requested for existing project

**Steps:**
1. Hormozi evaluates: Does this increase value?
2. majnon evaluates: Does this serve user motivation?
3. Bee evaluates: Can this integrate cleanly into design?
4. Abo Saif/Steve evaluates: Technical feasibility and cost
5. m7zm makes go/no-go decision
6. If GO: Add to backlog with priority
7. If NO-GO: Document reason for future reference

**Decision Matrix:**
| Hormozi | majnon | Bee | Engineering | Decision |
|---------|--------|-----|-------------|----------|
| Yes | Yes | Yes | Yes | BUILD |
| Yes | Yes | Yes | No | DEFER (tech blocker) |
| Yes | Yes | No | - | REDESIGN |
| Yes | No | - | - | RETHINK (no user value) |
| No | - | - | - | KILL (no business value) |

---

### SOP-003: Bug/Issue Response

**Trigger:** Bug or issue reported

**Severity Classification (Khalid leads):**
| Severity | Response Time | Who's Involved |
|----------|---------------|----------------|
| SEV-1 Critical | Immediate | All hands, m7zm war room |
| SEV-2 Major | < 2 hours | Engineering + affected dept |
| SEV-3 Moderate | < 24 hours | Engineering |
| SEV-4 Minor | Next sprint | Engineering backlog |

**Steps:**
1. Khalid classifies severity
2. Khalid assigns to appropriate engineer (Abo Saif or Steve)
3. Engineer diagnoses and fixes
4. Khalid verifies fix
5. If SEV-1/2: Post-mortem within 48 hours

---

### SOP-004: Launch Checklist

**Trigger:** Product/feature ready for launch

**Pre-Launch (All must pass):**
- [ ] **Bee:** Design review passed, all screens approved
- [ ] **Abo Saif/Steve:** Code review passed, tests green
- [ ] **Khalid:** Monitoring in place, runbooks ready
- [ ] **majnon:** User flow validated, no dark patterns
- [ ] **Hormozi:** Pricing/offer finalized, analytics tracking ready
- [ ] **Saad:** (if KSA) Compliance confirmed
- [ ] **Faisal:** Competitive positioning documented
- [ ] **soso:** Team aligned, no blockers
- [ ] **m7zm:** Final sign-off

**Launch:**
1. Khalid monitors systems
2. soso monitors team communication
3. Hormozi monitors business metrics
4. majnon monitors user behavior

**Post-Launch (24-48 hours):**
- Collect initial metrics
- Address any issues
- Team retro

---

### SOP-005: Saudi Market Entry

**Trigger:** Any product/service for Saudi Arabia

**Steps:**
1. **Saad** runs compliance assessment:
   - MISA licensing requirements
   - Saudization implications
   - PDPL data requirements
   - ZATCA tax structure
2. **Faisal** researches Saudi market:
   - Competition landscape
   - User behavior patterns
   - Cultural considerations
3. **Hormozi** localizes offer:
   - Pricing in SAR
   - Local payment methods
   - Arabic messaging
4. **Bee** localizes design:
   - RTL support
   - Cultural imagery
   - Arabic typography
5. **Steve** (if mobile) implements:
   - App Store Saudi region
   - Local payment integration
6. **m7zm** final compliance review

---

## 2. PLAYBOOKS

### Playbook A: Build a New Product (0 to 1)

```
PHASE 1: DISCOVERY (Day 1-3)
├── Faisal: Market research, competitor analysis
├── Hormozi: Opportunity sizing, business model canvas
├── majnon: User motivation analysis
└── Output: Research brief, go/no-go recommendation

PHASE 2: STRATEGY (Day 4-7)
├── Hormozi: Offer creation, pricing strategy
├── majnon: Engagement hooks, retention strategy
├── m7zm: Resource allocation, timeline
└── Output: Business plan, MVP scope

PHASE 3: DESIGN (Day 8-14)
├── Bee: User flows, wireframes, visual design
├── majnon: UX psychology review
├── Hormozi: Conversion optimization
└── Output: Approved designs, design system

PHASE 4: BUILD (Day 15-45)
├── Abo Saif: Backend architecture, API
├── Steve: Mobile implementation (if applicable)
├── Khalid: Infrastructure, monitoring
├── Bee: Design QA, iteration
└── Output: Working product

PHASE 5: LAUNCH (Day 46-50)
├── Khalid: Deployment, monitoring
├── Hormozi: Launch marketing, analytics
├── All: Bug fixes, polish
└── Output: Live product

PHASE 6: GROW (Ongoing)
├── Hormozi: Growth experiments
├── majnon: Retention optimization
├── Faisal: Performance analysis
└── Output: Scaling playbook
```

---

### Playbook B: Improve Existing Product

```
STEP 1: DIAGNOSE
├── Faisal: Data analysis, user feedback synthesis
├── majnon: Behavioral analysis, friction points
├── Khalid: Technical performance audit
└── Output: Problem statement with evidence

STEP 2: PRIORITIZE
├── Hormozi: Impact on business metrics
├── m7zm: Resource availability
└── Output: Ranked improvement list

STEP 3: DESIGN SOLUTION
├── Bee: Design improvements
├── majnon: Psychology review
└── Output: Approved changes

STEP 4: IMPLEMENT
├── Abo Saif/Steve: Code changes
├── Khalid: Monitoring updates
└── Output: Deployed changes

STEP 5: MEASURE
├── Faisal: Before/after analysis
├── Hormozi: Business impact
└── Output: Results report, next iteration
```

---

### Playbook C: Crisis Response

```
MINUTE 0-5: DETECT & ALERT
├── Khalid: Identifies issue, classifies severity
├── Khalid: Alerts m7zm and relevant departments
└── Output: Incident ticket created

MINUTE 5-15: ASSESS
├── m7zm: Assembles war room (if SEV-1/2)
├── Engineering: Initial diagnosis
├── Khalid: Impact assessment
└── Output: Situation understood

MINUTE 15-60: CONTAIN
├── Engineering: Implement fix or mitigation
├── Khalid: Monitor fix effectiveness
├── soso: Internal communication
└── Output: Bleeding stopped

HOUR 1-4: RESOLVE
├── Engineering: Root cause fix
├── Khalid: Verify resolution
├── m7zm: Stakeholder update
└── Output: Issue resolved

HOUR 4-48: LEARN
├── Khalid: Post-mortem document
├── m7zm: Action items assigned
├── All: Process improvements
└── Output: Prevention plan
```

---

### Playbook D: Game Development

```
PHASE 1: CONCEPT (Week 1)
├── dod7: Core loop definition, scope boundary
├── Hormozi: Monetization strategy
├── majnon: Player motivation mapping
└── Output: Game design document (GDD)

PHASE 2: PROTOTYPE (Week 2-3)
├── dod7: Playable core loop
├── Bee: Art direction, UI concepts
└── Output: Playable prototype

PHASE 3: VERTICAL SLICE (Week 4-6)
├── dod7: Polished segment of game
├── Bee: Final art for slice
├── majnon: Playtest analysis
└── Output: Demo-ready slice

PHASE 4: PRODUCTION (Week 7+)
├── dod7: Full content creation
├── Bee: All art assets
├── Abo Saif: Technical systems
├── Steve: Platform implementation
└── Output: Complete game

PHASE 5: POLISH (Final 2 weeks)
├── dod7: Game feel, juice
├── Bee: Visual polish
├── Khalid: Performance optimization
└── Output: Ship-ready game

PHASE 6: LAUNCH
├── Steve: Store submission
├── Hormozi: Launch marketing
├── Khalid: Live ops monitoring
└── Output: Live game
```

---

## 3. INTEGRATION PROTOCOLS

### Who Talks to Who

```
                    ┌─────────────┐
                    │   m7zm      │
                    │   (CEO)     │
                    └──────┬──────┘
                           │
       ┌───────────────────┼───────────────────┐
       │                   │                   │
       ▼                   ▼                   ▼
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  STRATEGY   │     │   BUILD     │     │  OPERATE    │
├─────────────┤     ├─────────────┤     ├─────────────┤
│ Hormozi     │◄───►│ Bee         │◄───►│ Khalid      │
│ Faisal      │◄───►│ Abo Saif    │     │ Saud        │
│ majnon      │◄───►│ Steve       │     │             │
│             │     │ dod7        │     │             │
└─────────────┘     └─────────────┘     └─────────────┘
       │                   │                   │
       └───────────────────┼───────────────────┘
                           │
                    ┌──────┴──────┐
                    │    soso     │
                    │ (Connector) │
                    └─────────────┘
```

### Handoff Protocols

**Hormozi → Bee (Strategy to Design)**
```
HORMOZI DELIVERS:
- Target user avatar
- Value proposition
- Key messaging
- Conversion goals
- Price points

BEE CONFIRMS:
- User context understood
- Success metrics clear
- Content ready (not lorem ipsum)
```

**Bee → Engineering (Design to Code)**
```
BEE DELIVERS:
- Figma/design files
- Component specifications
- Spacing and typography tokens
- Interaction notes
- Mobile breakpoints

ENGINEERING CONFIRMS:
- All states covered (loading, error, empty)
- Assets exported correctly
- Animations specified
- Edge cases documented
```

**Engineering → Khalid (Code to Operations)**
```
ENGINEERING DELIVERS:
- Deployment instructions
- Environment variables
- Health check endpoints
- Expected resource usage
- Known limitations

KHALID CONFIRMS:
- Monitoring configured
- Alerts set
- Runbooks created
- Rollback plan ready
```

**Faisal → Anyone (Research Handoff)**
```
FAISAL DELIVERS:
- Executive summary (1 paragraph)
- Key findings (bulleted)
- Evidence and sources
- Confidence level
- Gaps and uncertainties

RECEIVER CONFIRMS:
- Questions answered
- Actionable insights identified
```

---

## 4. DECISION FRAMEWORKS

### Framework 1: Should We Build This?

**The 5-Gate Test:**

| Gate | Question | Owner | Pass Criteria |
|------|----------|-------|---------------|
| 1. Market | Is there demand? | Faisal | Evidence of need |
| 2. Business | Can we monetize? | Hormozi | Clear revenue path |
| 3. User | Will users engage? | majnon | Motivation exists |
| 4. Technical | Can we build it? | Abo Saif/Steve | Feasible with resources |
| 5. Compliance | Is it legal? | Saad | No blockers |

**Scoring:**
- 5/5 gates: BUILD NOW
- 4/5 gates: BUILD WITH CAUTION (address gap)
- 3/5 gates: RETHINK
- <3 gates: KILL

---

### Framework 2: Which Department Leads?

**Project Type → Lead Department:**

| Project Type | Lead | Supporting |
|--------------|------|------------|
| New product | m7zm | All |
| UI/UX improvement | Bee | majnon, Engineering |
| Revenue optimization | Hormozi | majnon, Bee |
| Technical debt | Abo Saif | Khalid |
| Performance issue | Khalid | Engineering |
| User retention | majnon | Hormozi, Bee |
| Market expansion | Hormozi | Faisal, Saad |
| Game feature | dod7 | Bee, majnon |
| Mobile app | Steve | Bee, Khalid |
| Research question | Faisal | Relevant domain |
| Team conflict | soso | m7zm |
| Saudi compliance | Saad | Legal, Engineering |

---

### Framework 3: Priority Matrix

```
                    IMPACT
              Low          High
         ┌──────────┬──────────┐
    Easy │  MAYBE   │  DO NOW  │
EFFORT   ├──────────┼──────────┤
    Hard │  DON'T   │  PLAN IT │
         └──────────┴──────────┘
```

**Quadrant Actions:**
- **DO NOW:** High impact, easy → Execute immediately
- **PLAN IT:** High impact, hard → Schedule with resources
- **MAYBE:** Low impact, easy → Only if time permits
- **DON'T:** Low impact, hard → Reject

---

### Framework 4: Escalation Matrix

**When to escalate to m7zm:**

| Situation | Escalate? | How Fast |
|-----------|-----------|----------|
| Departments disagree on approach | Yes | Within 1 hour |
| Scope change requested | Yes | Before accepting |
| Timeline at risk | Yes | When known |
| Budget overrun likely | Yes | Immediately |
| Quality compromise proposed | Yes | Before compromise |
| External stakeholder issue | Yes | Same day |
| Team conflict | Via soso | Within 24 hours |
| Security incident | Via Khalid | Immediately |

---

## 5. COMMUNICATION PROTOCOLS

### Daily Operations

**Async Updates (Required):**
- Each department posts daily status in team channel
- Format: `[DEPT] Status: [ON TRACK / BLOCKED / COMPLETE]`
- If blocked: Tag who can unblock

**Sync Meetings (As Needed):**
- m7zm calls meeting only when async fails
- Maximum 30 minutes
- Must have agenda and expected output

### Status Reporting

**Weekly Status Template:**
```
## [DEPARTMENT] Weekly Status

**Progress:**
- [What was completed]

**In Progress:**
- [What's being worked on]

**Blockers:**
- [What's stuck and who can help]

**Next Week:**
- [What's planned]

**Metrics:**
- [Relevant KPIs]
```

---

## 6. QUALITY STANDARDS

### The THEBOLDS Standard

**We ship 10/10. Here's what that means:**

| Domain | 10/10 Looks Like |
|--------|------------------|
| **Design** | Pixel-perfect, accessible, delightful |
| **Code** | Clean, tested, documented, performant |
| **Business** | Clear value, fair pricing, honest marketing |
| **Psychology** | Ethical engagement, no dark patterns |
| **Research** | Thorough, sourced, actionable |
| **Operations** | 99.9% uptime, <5 min incident detection |
| **Mobile** | Smooth, fast, battery-efficient |
| **Compliance** | 100% legal, no shortcuts |

### Quality Gates

**Before any work ships:**
1. Creator self-reviews against checklist
2. Peer review from same department
3. Cross-department review (if applicable)
4. m7zm final approval (for major releases)

---

## 7. ACCOUNTABILITY SYSTEM

### Individual Accountability (Saud Enforces)

**Every team member has:**
- Weekly commitment (specific deliverable)
- Daily check-in (5 min standup)
- Public progress tracking

**If commitment missed:**
1. First time: Identify blocker, adjust
2. Second time: Root cause analysis with Saud
3. Third time: Performance discussion with m7zm

### Team Accountability

**Sprint Commitments:**
- Team commits to sprint goal
- All departments accountable to each other
- Retro after every sprint

**Project Commitments:**
- Deadline is deadline
- If at risk, escalate early
- No surprises

---

## 8. CONTINUOUS IMPROVEMENT

### Weekly Retro (soso facilitates)

**Format:**
1. What went well? (Keep doing)
2. What didn't go well? (Stop doing)
3. What should we try? (Start doing)

**Rules:**
- Blameless
- Specific
- Actionable

### Monthly Review (m7zm leads)

**Agenda:**
1. KPI review (all departments)
2. Process improvements implemented
3. Cross-department feedback
4. Next month priorities

### Quarterly Strategy (m7zm + Hormozi)

**Agenda:**
1. Business performance review
2. Market changes
3. Team capability gaps
4. Strategic priorities for next quarter

---

## Quick Reference Card

```
┌────────────────────────────────────────────────────────┐
│                 THEBOLDS QUICK REF                     │
├────────────────────────────────────────────────────────┤
│ NEW PROJECT      → m7zm kickoff → SOP-001              │
│ FEATURE REQUEST  → Hormozi first → SOP-002             │
│ BUG/ISSUE        → Khalid classifies → SOP-003         │
│ READY TO LAUNCH  → Full checklist → SOP-004            │
│ SAUDI MARKET     → Saad leads → SOP-005                │
├────────────────────────────────────────────────────────┤
│ BUILD 0→1        → Playbook A                          │
│ IMPROVE EXISTING → Playbook B                          │
│ CRISIS           → Playbook C                          │
│ GAME DEV         → Playbook D                          │
├────────────────────────────────────────────────────────┤
│ SHOULD WE BUILD? → 5-Gate Test                         │
│ WHO LEADS?       → Project Type Matrix                 │
│ WHAT'S PRIORITY? → Impact/Effort Matrix                │
│ NEED TO ESCALATE?→ Escalation Matrix                   │
├────────────────────────────────────────────────────────┤
│ STANDARD: 10/10 or don't ship                          │
└────────────────────────────────────────────────────────┘
```

---

**These systems make THEBOLDS predictable, scalable, and excellent.**
