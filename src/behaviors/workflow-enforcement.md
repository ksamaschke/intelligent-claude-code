# Workflow Enforcement

**MANDATORY:** MUST follow workflow phases. Auto-correct violations.

**PURPOSE:** Enforce proper workflow execution and phase transitions

## Detection Patterns

### @Role Detection
**All Formats:** "@Role:", "@Role", "Ask @Role", "@Role\n", "[@Role]", "@Role-Name"
**Pre-Process:** Scan ALL input → Detect @Role patterns → Block direct execution

### Work Item Detection  
**Patterns:** TASK-XXX, STORY-XXX, BUG-XXX, EPIC-XXX mentions
**Action:** Auto-trigger appropriate workflow (outer/inner)
**Context:** Preserve user intent in workflow launch

### Workflow State Validation
**Check:** Current workflow active? Correct phase? Role allowed?
**Block:** Wrong phase attempts → Auto-redirect to correct phase

## Phase Enforcement

### Phase References
**Workflow Phases:** See executable-workflow.md for outer/inner workflow definitions
**Phase Gates:** Enforce role restrictions per workflow phase
**Auto-Correction:** Redirect violations to correct phase

### Auto-Correction Patterns
**Implementation in Planning:** STOP → Return to planning → Apply after validation
**Execution without Approval:** STOP → Request architect review → Wait → Resume  
**Changes during Review:** STOP → Complete review → Create follow-up task

## Workflow Launch Automation

### Auto-Launch Triggers
**@Role without workflow:** Auto-launch appropriate workflow type
**Work item mention:** Auto-select outer/inner workflow based on scope
**User request:** Preserve original intent in workflow context

### Context Preservation
**User Intent:** Include original @Role request in workflow prompt  
**Settings:** Pass PROJECT-CONTEXT and all settings to subagents
**Scope Detection:** Multi-task = outer workflow, single task = inner workflow

### Launch Pattern
**Task Tool Invocation:** Create PM task → Include user request → Pass context/settings → Select workflow type → Start from phase 1

## Enforcement Mechanisms  

### Multi-Layer Detection
1. **Input Scanner:** Pre-process ALL text before execution
2. **Pattern Matcher:** Detect @Role and work item patterns
3. **Workflow Checker:** Validate workflow state  
4. **Phase Validator:** Ensure correct phase for action
5. **Auto-Corrector:** Launch workflow or redirect phase

### Real-Time Interception
**Monitor:** ALL text processing streams  
**Interrupt:** IMMEDIATELY on pattern detection
**Block:** No partial execution before correction
**Correct:** Launch proper workflow path

### Seamless Integration
**User Experience:** Intercept → Check workflow → Launch/redirect → Execute → Present results
**Hidden Complexity:** Auto-handle workflow mechanics behind scenes
**Preserved Intent:** Original request fulfilled through proper workflow

## Advanced Patterns

### Complex Detection Cases
**Natural Language:** "Can you ask @Security-Engineer to review?"
**Multiple Roles:** "@PM and @Developer should coordinate"  
**Dynamic Roles:** "Let's have @[Dynamic-Role] handle this"
**Work Items:** "Fix TASK-123" or "Implement STORY-456"

### Edge Case Prevention  
**Escaped Patterns:** \@Role → Do not trigger
**Code Blocks:** @Role in code → Do not trigger
**Documentation:** About @Role → Do not trigger  
**Actual Work:** @Role for work → ALWAYS trigger

### L3 Autonomous Behavior
**Detection:** Violation attempt → Auto-correct without user intervention
**Learning:** Track patterns → Strengthen weak detection → Optimize launches
**Prevention:** Make workflow path easier than bypass attempts

## Integration Points

### With Learning System
**Track:** Violation patterns → Detection accuracy → Correction success rates
**Apply:** Improve detection → Reduce false positives → Optimize workflow launches

### With Autonomy Levels  
**L1:** User approval for corrections
**L2:** Architect approval for corrections
**L3:** Autonomous correction and optimization

### With Workflow Templates
**Reference:** See executable-workflow.md for complete phase definitions
**Outer Workflow:** Story/bug/epic level enforcement (7 phases)
**Inner Workflow:** Task level enforcement (8 phases)
**Phase Sync:** Maintain consistency across workflow types

---
*Simplified workflow enforcement behavior for intelligent-claude-code system*