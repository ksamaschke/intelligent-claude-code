# Git Safety & Privacy Behaviors

## Commit Privacy

### Remove AI Assistant Mentions
**Default**: Enabled (configure in config.md)

Never include in commits:
- "Claude", "AI", "Assistant" references
- "Generated by", "Created with" attributions
- Tool-specific mentions

**Instead of**: "Fixed bug with Claude's help"
**Use**: "Fixed authentication validation bug"

**Instead of**: "AI-generated test suite"
**Use**: "Added comprehensive test coverage"

## Sensitive Data Protection

### Automatic .gitignore Generation
**Default**: Enabled (configure in config.md)

Automatically add to .gitignore:
```
# Environment files
.env
.env.*
!.env.example

# Secrets and keys
*.key
*.pem
*.p12
*.pfx
secrets/
credentials/

# IDE and system
.idea/
.vscode/
*.swp
.DS_Store
Thumbs.db

# Build and dependencies
node_modules/
venv/
__pycache__/
*.pyc
dist/
build/

# Logs and databases
*.log
*.sqlite
*.db

# Temporary files
*.tmp
*.temp
.cache/
```

### Commit Validation
**Default**: Enabled (configure in config.md)

Before EVERY commit:
1. Scan for patterns:
   - API keys: `[A-Z0-9]{20,}`
   - AWS keys: `AKIA[0-9A-Z]{16}`
   - Private keys: `-----BEGIN.*PRIVATE`
   - Passwords: `password.*=.*['"]`
   - Tokens: `token.*=.*['"]`

2. Check files:
   - No .env files
   - No credential files
   - No private keys

3. If found:
   - Block commit
   - List violations
   - Suggest fixes

## CLAUDE.md Privacy

### Gitignore Project CLAUDE.md
**Default**: Disabled (configure in config.md)

When enabled:
- Adds `CLAUDE.md` to .gitignore
- Keeps project-specific instructions private
- Still tracks ~/.claude/CLAUDE.md

## Commit Message Standards

### Human-Like Messages
**Default**: Enabled (configure in config.md)

**Guidelines**:
- Concise and specific
- Present tense imperative
- No exaggeration or fluff
- Focus on "what" and "why"

**Good Examples**:
```
Add user authentication endpoints
Fix memory leak in data processor
Refactor database connection logic
Update dependencies to latest versions
```

**Avoid**:
```
Massively improve incredible authentication system
Revolutionize the way we handle data
Brilliantly refactor for optimal performance
```

### Commit Structure
```
<type>: <subject>

<body (optional)>

<footer (optional)>
```

Types: feat, fix, docs, style, refactor, test, chore

## Icon and Emoji Control

### No Icons Mode
**Default**: Disabled (configure in config.md)

When enabled:
- No emojis in commits
- No icons in documentation
- No decorative symbols
- Plain text only

**With icons**: "✨ Add new feature"
**Without icons**: "Add new feature"

## Automatic Cleanup

### File Organization  
**Default**: ALWAYS ON (configure in config.md)
**Note**: This is a core hygiene rule - always active

**Temporary File Cleanup**:
- Remove: `*.tmp`, `*.temp`, `*.bak`
- Clean: empty directories
- Delete: test artifacts

**Progress File Management**:
- Archive completed progress files
- Move to `.archive/` directory
- Keep last 5 versions

**Semantic Organization**:
```
project/
├── src/           # Source code
├── tests/         # Test files
├── docs/          # Documentation
├── scripts/       # Build/utility scripts
├── config/        # Configuration files
└── .archive/      # Archived progress files
```

**Auto-organize**:
- Move tests to tests/
- Move docs to docs/
- Group configs in config/
- Sort imports alphabetically

## Configuration

Configure these behaviors in your config.md:

```markdown
# Git Privacy & Safety Configuration
- git_privacy: true              # Remove AI mentions from commits
- auto_gitignore: true           # Auto-generate .gitignore
- validate_commits: true         # Check for sensitive data
- gitignore_project_claude: false # Add CLAUDE.md to .gitignore
- human_commits: true            # Human-like commit messages
- no_icons: false               # Disable emojis/icons
- auto_cleanup: true            # Clean temporary files

# Cleanup Configuration
- cleanup_patterns: "*.tmp,*.temp,*.bak"  # Files to clean
- archive_progress: true         # Archive progress files
- organize_files: true          # Semantic file organization
```

## Natural Overrides

- "Include my name in the commit" → Allows attribution
- "Keep the temporary files" → Skips cleanup
- "Don't reorganize" → Maintains current structure
- "Use emojis this time" → Enables icons temporarily

## Safety Workflow

1. **Before changes**: Check current branch
2. **Before commit**: 
   - Validate no secrets
   - Generate human-like message
   - Remove AI mentions
3. **After commit**: 
   - Clean temporary files
   - Organize if needed
4. **Periodically**: 
   - Update .gitignore
   - Archive old progress