# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2026-02-06

### Added
- Parallel subagent execution for significantly faster analysis
- 3-phase execution model: Discovery → Parallel Analysis → Synthesis
- 5 simultaneous subagents: Stage Detection, Token Analysis, Stale Docs, Semantic Sync, Ecosystem Analysis
- Adaptive mode: fewer subagents for small projects without docs/

### Changed
- Analysis steps restructured from sequential to parallel execution
- Added Task and Bash to allowed-tools for subagent orchestration

## [1.0.0] - 2026-02-06

### Added
- Initial release as installable Claude Code marketplace plugin
- 8 analysis modes: analyze, optimize, apply, compare, create, sync, audit, scaffold
- 10 anti-pattern detection (context stuffing, stale docs, orphan files, code-doc drift, etc.)
- Semantic sync analysis between code and documentation
- Project stage detection (INIT / ACTIVE / STABLE / MAINTENANCE)
- Token analysis with target benchmarks (2.5k ideal, 4k max)
- Documentation ecosystem mapping and link graph analysis
- Deep Dive link recommendations for CLAUDE.md
- docs/ scaffold generation based on project stage
- MIT + Commons Clause license

[1.1.0]: https://github.com/kojott/claude-docu-optimizer/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/kojott/claude-docu-optimizer/releases/tag/v1.0.0
