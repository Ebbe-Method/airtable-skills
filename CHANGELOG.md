# Changelog

All notable changes to the Airtable Skills plugin.

## [1.4.0] - 2026-02-08

### Added

- **Auto-release on git push** - New Claude Code hook recipe in the `airtable-extensions` skill that automatically runs `block release` after every `git push`, keeping your Airtable extension in sync with your GitHub repo
  - PostToolUse hook detects `git push` commands scoped to your extension repo
  - Skips release if the push failed
  - Step-by-step setup instructions included in the skill

## [1.3.0] - 2026-02-05

### Added

- **New skill: `/airtable-base-audit`** - Comprehensive base health analysis
  - Field Health (~35%): Unused fields, low fill rates, "(copy)" fields, uniqueness analysis
  - Performance (~35%): Record count vs plan limits, TODAY() formula detection, complex formulas
  - Schema Quality (~30%): Repeated data patterns, missing relationships, denormalization
  - Letter grade (A-F) scoring with percentage breakdown
  - Three output modes: apply safe fixes, export report, detailed recommendations
  - Plan-aware limits (Teams/Business/Enterprise)

## [1.2.0] - 2026-02-05

### Added

- **Claude Cowork compatibility** - Plugin now works in both Claude Code CLI and Claude Cowork web
- **Bundled MCP configuration** - `.mcp.json` auto-configures Airtable MCP server on install
- Added `cowork` keyword for marketplace discovery
- Added `homepage` and `repository` fields to plugin manifest

### Documentation

- Updated README with Cowork installation instructions
- Added airtable-field-audit skill to README skills table

## [1.1.0] - 2026-02-05

### Added

- **New skill: `/airtable-field-audit`** - Analyze and clean up field naming issues
  - Detects whitespace (leading/trailing spaces)
  - Finds near-duplicates (typos, hyphen variations)
  - Flags similar/confusing names (Status vs Status 2)
  - Identifies inconsistent casing (firstName vs FirstName)
  - Three remediation modes: auto-fix, review each, export report
  - Respects emoji prefix conventions (won't flag `[email] Email` as duplicate)

### Documentation

- Added brainstorm: `docs/brainstorms/2026-02-05-field-audit-brainstorm.md`
- Added implementation plan: `docs/plans/2026-02-05-feat-airtable-field-audit-skill-plan.md`

## [1.0.0] - 2026-02-04

### Added

- Initial release
- **Skill: `airtable`** - Comprehensive Airtable assistant for schema design, API interactions, scripting, interfaces, and automations
- **Skill: `airtable-extensions`** - Custom React extensions development
- Reference documentation for field types, API patterns, MCP patterns, scripting, automations, and more
