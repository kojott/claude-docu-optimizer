# claude-docu-optimizer

A Claude Code plugin for optimizing `CLAUDE.md` files and the `docs/` documentation ecosystem following battle-tested patterns from Boris Cherny's team at Anthropic.

## What it does

Analyzes and optimizes your project documentation to keep Claude Code's context efficient and your docs synchronized with code.

**Key features:**
- Token analysis with target benchmarks (2.5k ideal, 4k max)
- 10 anti-pattern detection (context stuffing, stale docs, orphan files, code-doc drift...)
- Semantic sync analysis between code and documentation
- Project stage detection (INIT / ACTIVE / STABLE / MAINTENANCE)
- Documentation ecosystem mapping and link graph analysis

## Modes

| Mode | Description |
|------|-------------|
| `analyze` | Report issues only (default) |
| `optimize` | Full analysis + optimized version |
| `apply` | Directly update the file |
| `compare` | Before/after with token savings |
| `create` | Generate new CLAUDE.md from project structure |
| `sync` | Semantic check of docs ↔ code synchronization |
| `audit` | Complete audit of documentation ecosystem |
| `scaffold` | Generate docs/ structure for new project |

## Installation

Add the marketplace and install the plugin:

```bash
claude plugin marketplace add https://github.com/kojott/claude-docu-optimizer
claude plugin install docu-optimizer@claude-docu-optimizer
```

### Updating

```bash
claude plugin marketplace update claude-docu-optimizer
claude plugin update docu-optimizer@claude-docu-optimizer
```

## Usage

```
/docu-optimizer analyze     # Report issues
/docu-optimizer optimize    # Full analysis + optimized version
/docu-optimizer apply       # Directly update CLAUDE.md
/docu-optimizer compare     # Before/after comparison
/docu-optimizer create      # Generate new CLAUDE.md
/docu-optimizer sync        # Check docs ↔ code sync
/docu-optimizer audit       # Full documentation ecosystem audit
/docu-optimizer scaffold    # Generate docs/ structure
```

## Target metrics

| Metric | Value |
|--------|-------|
| Ideal CLAUDE.md size | ~2.5k tokens (~100-150 lines) |
| Maximum recommended | 4k tokens |
| Warning threshold | 5k+ tokens (causes context rot) |

## Anti-patterns detected

1. **Context Stuffing** - Verbose, redundant instructions
2. **Static Memory** - No evolution/learnings section
3. **Missing Plan Mode Guidance** - No workflow section
4. **No Verification Loop** - No test commands specified
5. **Permissions Not Documented** - Team environments only
6. **No Format Standards** - Missing formatting hooks
7. **Stale Documentation** - Docs don't match code
8. **Missing Index** - No docs/README.md
9. **Orphan Docs** - Unreferenced documentation files
10. **Code-Doc Drift** - API signatures out of sync

## License

MIT + Commons Clause - Free to use, modify, and share. Commercial selling requires author's approval. See [LICENSE](LICENSE) for details.
