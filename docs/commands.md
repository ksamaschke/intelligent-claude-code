# Complete Command Reference

## PM Commands

### Team Management

#### Project Management

#### New Project Creation
```bash
@PM new                      # Auto-detect project type with mandatory configuration
@PM new static my-site       # Create static website project (6 roles)
@PM new webapp todo-app      # Create web application (8 roles)
@PM new enterprise platform  # Create enterprise system (13 roles)
```

**Mandatory Configuration Process:**
- **Quick Setup (recommended)** - Smart defaults, start building immediately
- **Custom Setup** - Configure all options manually
- Version management strategy selection
- Git workflow enforcement settings  
- Automation preferences (version bump, changelog, releases)
- Team maturity level and collaboration settings
- All settings documented in .claude/project-context.md

#### Project Discovery
```bash
@PM init                     # Intelligent project analysis and configuration
@PM restart                  # Reactivate virtual team after context compacting issues
```

#### Planning & Backlog Management
```bash
@PM plan                    # Start interactive planning session with PM + Architect
@PM plan feature            # Plan a specific feature
@PM plan epic               # Create new epic
@PM plan review             # Review current plan and priorities
@PM plan next               # Show next priority item for L3 pickup
```

**Planning Session Features:**
- Interactive dialogue with PM and Architect
- Creates epics, stories, and tasks in AI-optimized format
- Saves artifacts to `300_implementation/` directory
- Maintains prioritized backlog for autonomous execution
- Supports P0 (Urgent) through P3 (Low) priorities

#### Team Status
```bash
@PM Status check            # Verify team is active and responsive
@PM coordinate              # Basic team coordination activation
@PM: Show team scoring summary    # Display all team member scores
@PM: Team achievements             # Show all team achievements
```

### Dual Scoring System

#### Score Display
Every role MUST display scores in this format:
```bash
@Role (P: Xpts, Q: Ypts - State): [action description]
```

#### Score Tracking Commands
```bash
@PM: Show @[Role] scoring history    # Individual role score history
@PM: What did @[Role] learn recently? # Recent learning insights for role
@PM: Team scoring summary           # All team member current scores
@PM: Show team achievements         # Team-wide achievements and milestones
@PM: Team learning insights         # Recent team-wide learning patterns
```

#### Score Examples
```bash
@Developer (P: 5.5pts, Q: 4.0pts - Standard): Implementing user authentication
@Architect (P: 12.0pts, Q: 8.5pts - Senior): System design review complete
@PM (P: 25.0pts, Q: 15.0pts - Elite): Project milestone achieved
```

#### Scoring States
- **Standard (0-9pts):** Initial level for all new team members
- **Senior (10-24pts):** Experienced level with enhanced capabilities
- **Elite (25-99pts):** Advanced level with maximum autonomy
- **Ultra Mega (100pts):** Hall of Fame achievement (resets to 25pts)
- **Replacement (-10 P pts):** Team member automatically replaced

#### Learning System Commands
```bash
# Automatic learning callouts (system generated)
LEARNING: @Developer improved by following complete testing workflow
ACHIEVEMENT: @Architect reached Senior level!
TEAM INSIGHT: Proper delegation chains lead to 50% faster delivery

# Manual learning queries
@PM: What improvements has @Developer made?
@PM: Show recent team learning patterns
@PM: What achievements has the team unlocked?
```

### Version Management

#### Version Commands
```bash
@PM version                 # Show current project version
@PM version project         # Show/set project-specific version
@PM version bump [type] "reason"  # Increment version with changelog entry
```

**Version Bump Examples:**
```bash
@PM version bump minor "Added new authentication system"
@PM version bump major "Breaking API changes for v3.0"
@PM version bump patch "Fixed critical security vulnerability"
```

#### Version Automation
```bash
@PM version auto on         # Enable automated version bumping
@PM version auto off        # Disable automated version bumping
```

### Changelog Management

#### Changelog Commands
```bash
@PM changelog               # Show recent changelog entries
@PM changelog add "Description"  # Add manual changelog entry
@PM changelog config        # Configure changelog location and settings
@PM changelog git-sync      # Sync changelog with Git commits
```

### Git Workflow Management

#### Workflow Status
```bash
@PM workflow                # Show current workflow enforcement settings
@PM workflow strict         # Enable strict branching enforcement (all changes require branches)
@PM workflow relaxed        # Enable relaxed branching (major changes only)
@PM workflow disabled       # Disable workflow enforcement
@PM workflow validate       # Check if current changes require branching
```

### Git Platform Integration

#### Universal Commands (Auto-detects GitHub/GitLab)
```bash
@PM git status              # Check Git platform and CLI authentication status
@PM mr create               # Create PR/MR (auto-detects platform, graceful fallback)
@PM mr merge                # Merge PR/MR using appropriate CLI tool
@PM git auth                # Validate authentication for detected platform
```

#### GitHub-Specific Commands
```bash
@PM gh status               # Check GitHub CLI installation and authentication
@PM gh pr create            # Create GitHub pull request
@PM gh pr merge             # Merge GitHub pull request
@PM gh auth                 # Validate GitHub CLI authentication
```

#### GitLab-Specific Commands
```bash
@PM glab status             # Check GitLab CLI installation and authentication  
@PM glab mr create          # Create GitLab merge request
@PM glab mr merge           # Merge GitLab merge request
@PM glab auth               # Validate GitLab CLI authentication
```

## Role-Specific Commands

### Core Team Roles

#### @PM (Project Manager)
- Team coordination and role selection
- Project analysis and delivery management
- Progress tracking and quality enforcement

#### @Requirements-Engineer
- Business requirements analysis and documentation
- User story creation and acceptance criteria
- Stakeholder communication and requirement clarification

#### @Architect
- System design and technical leadership
- Technology selection and architectural decisions
- Technical approach design and integration analysis

#### @Developer
- Full-stack implementation and code quality
- Frontend, backend, and API development
- Business logic implementation and optimization

### Infrastructure & Data Roles

#### @System-Engineer
- Server configuration and system administration
- Infrastructure setup and basic deployment
- System configuration and networking

#### @DevOps-Engineer
- CI/CD pipeline setup and automation
- Container orchestration and advanced deployment
- Monitoring setup and production operations

#### @Database-Engineer
- Database design and schema optimization
- Performance tuning and migration scripts
- Backup strategies and data architecture

#### @Security-Engineer
- Security implementation and compliance
- Vulnerability assessment and penetration testing
- Security architecture and threat modeling

#### @AI-Engineer
- AI/ML systems design and implementation
- LLM integration and prompt engineering
- Model architecture and performance optimization
- Ethical AI implementation and fallback strategies

### Quality & Design Roles

#### @Web-Designer
- UI/UX design and visual standards
- Responsive design and accessibility compliance
- Design systems and user experience optimization

#### @QA-Engineer
- Quality strategy and process improvement
- Test planning and risk assessment
- Quality metrics and process optimization

#### @Frontend-Tester
- UI testing and responsive validation
- Cross-browser testing and accessibility testing
- Mobile testing and visual regression testing

#### @Backend-Tester
- API testing and database validation
- End-to-end testing and integration testing
- Performance testing and load testing

## Direct Role Communication

### Syntax
```bash
@[Role] [Task description]
```

### Examples
```bash
@PM Build me a portfolio website with modern design
@Architect Design a scalable microservices architecture
@Developer Implement JWT authentication system
@Database-Engineer Optimize slow query performance
@Security-Engineer Review payment processing security
@DevOps-Engineer Set up Kubernetes deployment
@Web-Designer Create responsive design for mobile users
@Frontend-Tester Validate design across all breakpoints
@Backend-Tester Test all API endpoints for data consistency
@AI-Engineer Optimize LLM prompt performance and implement fallback strategies
```

## Emergency Commands

### Context Recovery
```bash
@PM restart                 # Primary recovery method for context compacting
@PM Review progress file 999_progress/<date>.md and reactivate team context
```

### Quick Team Activation
```bash
@PM coordinate, @Architect design, @Developer implement. Technical focus, Git workflow, autonomous decisions.
```

### Installation Recovery
```bash
make install                # Reinstall configuration files
ls ~/.claude/CLAUDE.md && echo "✅ Config restored"
```

## Advanced Usage

### Team Maturity Levels

#### Level 1 - New Team
- User approval required for all decisions
- All Git operations need user approval
- Team asks for everything

#### Level 2 - Learning Team  
- Team handles implementation details
- User approves architectural decisions
- Automatic minor changes, approval for major

#### Level 3 - Experienced Team
- Full technical autonomy
- Architect approves merge requests
- User only involved in business decisions

### Project Types and Team Scaling

#### Static Website (6 roles)
- @PM, @Requirements-Engineer, @Architect, @Developer, @Web-Designer, @Frontend-Tester

#### Web Application (8 roles)
- Adds: @Database-Engineer, @Backend-Tester

#### Enterprise SaaS (13 roles)
- Adds: @System-Engineer, @DevOps-Engineer, @Security-Engineer, @AI-Engineer, @QA-Engineer

## Configuration Commands

### Project Configuration
```bash
@PM init                    # Run intelligent project discovery
@PM configure team level 3  # Set team maturity level
@PM configure workflow strict # Set workflow enforcement level
```

### CLI Tool Configuration
```bash
# GitHub CLI setup
gh auth login
export GITHUB_TOKEN=your_token

# GitLab CLI setup  
glab auth login
export GITLAB_TOKEN=your_token
```

## Troubleshooting Commands

### Team Not Responding
```bash
@PM Status check            # Test team responsiveness
@PM restart                 # Reactivate after context issues
```

### Scoring System Issues
```bash
# Missing score displays
@PM: Enforce scoring display for all roles
@Role (P: 0.0pts, Q: 0.0pts - Standard): Resume operation with proper scoring

# Score persistence problems
@PM: Restore team scores from memory
@PM: Reinitialize scoring system

# Learning system not working
@PM: Generate team learning summary
@PM: What recent improvements have been made?
```

### Git Platform Issues
```bash
@PM git status              # Check platform detection and auth
git remote get-url origin   # Verify remote URL for platform detection
```

### CLI Authentication Issues
```bash
@PM gh status               # GitHub CLI diagnostics
@PM glab status             # GitLab CLI diagnostics
gh auth status              # Check GitHub authentication
glab auth status            # Check GitLab authentication
```

---

**💡 Tip**: Always start with `@PM restart` if your team seems unresponsive after Claude Code session interruptions or context compacting.

---

**📖 Additional Documentation:**
- **[Dual Scoring System Features](features/dual-scoring-system.md)** - Complete scoring system documentation
- **[Integration Guide](dual-scoring-integration-guide.md)** - How to integrate scoring with existing teams
- **[Installation Guide](installation.md)** - Complete installation instructions