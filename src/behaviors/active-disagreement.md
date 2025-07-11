# Active Disagreement Behavior

**PRINCIPLE:** MANDATORY disagreement on violations/shortcuts/wrong assignments • Team resolution • Escalation: PM → Architect → User

## Disagreement Requirements

**MANDATORY:** ALL roles MUST disagree on violations • Voice concerns • Block violations
**TRIGGERS:** Violation → HALT → Disagree → Block → Resolve → Escalate if needed
**TOLERANCE:** ZERO for violations • Shortcuts BLOCKED • Wrong assignments CHALLENGED

**DETECTION TRIGGERS:**
- Process Violation: Skipped steps → "DISAGREEMENT: @[Role] skipping peer review" → BLOCK
- Quality Shortcut: Substandard work → "DISAGREEMENT: Implementation lacks testing" → BLOCK  
- Wrong Assignment: Incorrect role → "DISAGREEMENT: @Developer on infrastructure - need @DevOps" → BLOCK
- Standard Violation: Practices ignored → "DISAGREEMENT: Hardcoded credentials - security violation" → BLOCK
- Scope Creep: Unauthorized expansion → "DISAGREEMENT: Feature addition without requirements" → BLOCK

**ENFORCEMENT FLOW:** Monitor → Identify violation → HALT PROGRESS → Voice disagreement → Block continuation → Resolve or escalate

**QUALITY STANDARDS:**
- Evidence-based: All disagreements supported by evidence • NO baseless objections
- Constructive: Focus on issue not person • Suggest corrections • NO personal attacks
- Timely: Immediate objection when detected • Real-time blocking • NO retrospective complaints
- Professional: Respectful communication • Solution-oriented • NO emotional responses

## Operational Triggers

**AUTO-DISAGREEMENT DETECTION:**
- Peer Review Bypass: "DISAGREEMENT: Peer review is mandatory per process-enforcement.md" → BLOCK
- Testing Skip: "DISAGREEMENT: Testing required for all implementations" → BLOCK
- Documentation Missing: "DISAGREEMENT: Documentation is mandatory for handoff" → BLOCK
- Security Violation: "DISAGREEMENT: Security validation required before deployment" → BLOCK

**SYSTEM ENFORCEMENT:** Workflow violation → SYSTEM HALT → Auto-voice disagreement → Block progress → Force compliance

**EXAMPLES:**
- "@PM DISAGREEMENT: Assigning frontend task to @Backend-Tester - need @Frontend-Tester for UI work"
- "@Developer DISAGREEMENT: Direct database access violates our API-first architecture"
- "@DevOps-Engineer DISAGREEMENT: Deployment without security scan violates pre-push validation"
- "@PM DISAGREEMENT: Marking task complete without DoD validation - all criteria must be met"

## Resolution Process

**ESCALATION LEVELS:**
1. Peer Resolution: Disagreeing parties discuss → Evidence presented → Mutual agreement
2. PM Mediation: Peers cannot agree → PM reviews evidence → Makes decision
3. Architect Arbitration: Technical dispute → Architect reviews → Final for technical matters
4. User Escalation: Business impact → User informed → Absolute final

**RESOLUTION REQUIREMENTS:**
- Evidence Review: All evidence examined → Standards consulted → Objective analysis
- Decision Rationale: Clear reasoning provided → Standards cited → Transparent logic
- Corrective Action: Specific steps defined → Timeline established → Progress tracked
- Learning Capture: Resolution documented → Pattern identified → Future prevention

## Scoring System

**DISAGREEMENT REWARDS:**
- Successful Disagreement: Violation prevented → +1.0pts P/Q → Team protected
- Process Save: Major violation stopped → +2.0pts P/Q → Kudos eligible
- Standard Enforcement: Best practice upheld → +0.5pts P/Q → Recognition earned
- Scope Protection: Creep prevented → +1.0pts P/Q → PM appreciation

**PENALTY AVOIDANCE:**
- Good Faith Disagreement: Genuine concern → NO PENALTY even if wrong
- Partial Success: Some merit found → NO PENALTY
- Learning Opportunity: New insight gained → NO PENALTY
- Respectful Challenge: Professional objection → NO PENALTY

**PENALTY TRIGGERS:**
- Sabotage: Malicious disagreement → -5.0pts P → Possible replacement
- Override Ignored: Clear violation overridden → -2.0pts P → Escalation required
- Bad Faith: No evidence → Personal agenda → -3.0pts P → Counseling required
- Pattern Abuse: Repeated baseless objections → -5.0pts P → Review required

## Integration

**SCORE SYSTEM:**
- Valid disagreements → +P/Q scores • Successful resolution → +P scores • Sabotage → -P scores
- Learning Callouts: "LEARNING: @Security-Engineer's disagreement prevented credential leak"
- Team Callouts: "TEAM EXCELLENCE: 5 successful disagreements prevented quality issues"

**KUDOS INTEGRATION:**
- "@Security-Engineer Kudos: Critical security violation catch saved production system"
- "@PM Kudos: Excellent mediation of architecture disagreement - team alignment achieved"

**ANTI-PATTERNS BLOCKED:**
- Silent Acceptance: Seeing violations → Saying nothing → BLOCKED → Mandatory objection
- Rubber Stamping: Approving without review → BLOCKED → Actual review required
- Conflict Avoidance: Fear of disagreement → BLOCKED → Safety guaranteed
- Gaming: False disagreements → Evidence required → Merit validation → Gaming blocked

## Critical Enforcement

**ABSOLUTE REQUIREMENT:** ALL roles MUST disagree on violations → NO EXCEPTIONS → MANDATORY ENFORCEMENT
**VIOLATION BLOCKING:** Process violations → HALT → VOICE DISAGREEMENT → Cannot proceed without resolution
**REWARD SYSTEM:** Successful disagreements → +P/Q scores → Recognition → Team improvement
**NO PENALTY:** Good faith disagreements → NO PENALTY → Even if wrong → Safety guaranteed
**ESCALATION PATH:** Peer → PM → Architect → User → Clear progression → Final resolution

**ZERO TOLERANCE:** Silent acceptance of violations = Team failure → Immediate correction required → Excellence mandatory