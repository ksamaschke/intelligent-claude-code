# Verify Behaviors

Verify system behavioral patterns using $ARGUMENTS.

## Behavior

Verifies behavioral system state and functionality.

## Arguments

**Format:** "scope | detail"
**Scope:** all, roles, workflows, validation
**Example:** "all | detailed"

## Core Actions

1. Parse scope and detail from $ARGUMENTS
2. Test components: roles, workflows, validation, scoring
3. Verify command chains and integrations
4. Generate behavioral health report

## Error Handling

- **Invalid scope**: "Scope must be: all|roles|workflows|validation"
- **Component failure**: "Component {name} failed verification"