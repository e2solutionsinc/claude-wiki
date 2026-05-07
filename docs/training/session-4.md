# Session 4 — SQL and Stored Procedures

**Format:** 45-60 min | **Tool:** Claude Code or Claude.ai Web

## Agenda

1. Giving Claude the right context for SQL work (schema, platform, conventions)
2. Briefly discuss how Claude uses the sproc template and coding examples (wiki reference: [T-SQL Claude.ai Web](../tsql-ssms.md), [T-SQL Claude Code](../tsql-claude-code.md))
3. Live demo: prompt Claude to build a sproc from a plain English description
4. Live demo: paste an existing sproc, ask Claude to add error handling or a new param
5. Prompting tips specific to T-SQL (wiki reference: [Best Practices](../best-practices.md), [T-SQL Automated Testing](../tsql-automated-testing.md))

## Talking Points

- Always tell Claude the DB name, platform (WebWise/Advantage Architect), and relevant tables
- Paste `CREATE TABLE` scripts for the tables involved — Claude needs to know the columns
- Use `@in_debug = 'YES'` pattern for development and production troubleshooting
- `@error_tag` pattern — set a unique tag before each statement so failures are traceable in `t_error_log`
- Claude won't know about `t_log_control`, `t_error_log`, etc. unless you tell it — that's what the CLAUDE.md is for
