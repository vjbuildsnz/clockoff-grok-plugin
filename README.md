# ClockOff for Grok

One packaged plugin: eight shared skills and the ClockOff remote MCP connection.
Install the package together rather than copying one skill and configuring a
separate connector by hand. No marketplace listing or directory approval is
needed to distribute these files.

## Get the package

- Git repository: https://github.com/vjbuildsnz/clockoff-grok-plugin
- Versioned ZIP and SHA-256 checksum: https://github.com/vjbuildsnz/clockoff-grok-plugin/releases

The repository root is the plugin root. A ZIP has the same root layout:

```text
plugin.json
mcp.json
skills/
  clockoff/SKILL.md
  setup/SKILL.md
  gym-daily/SKILL.md
  gym-members/SKILL.md
  gym-classes/SKILL.md
  gym-followups/SKILL.md
  gym-campaigns/SKILL.md
  gym-review/SKILL.md
```

## Load and connect

**Grok Bot:** use its supported private plugin installation/import flow under
Connect apps → Your plugins. It is listed as an Agent Plugins client supporting
skills and Streamable HTTP MCP. If the client offers a Git source, use the
repository URL; if it offers file import, use the release ZIP. The exact custom
Git/ZIP import controls have not been verified in a signed-in Grok Bot account;
this repository does not invent a one-click install URL or a command for them.

**Grok Build:** its documented local plugin loader accepts a directory through
`--plugin-dir <PATH>` or `~/.grok/plugins/`. Clone this repository and give the
plugin directory to that loader. This is the coding agent, a separate Grok
surface from Grok Bot and grok.com chat.

Complete ClockOff sign-in through the host's secure OAuth flow. Reuse an existing
ClockOff connection if the host supports it; do not duplicate the gym connection
or copy credentials into this repository, a download URL or chat. Package loading
does not sign in, enable monitoring or start a routine.

Ask **Start ClockOff**, then **Who am I connected as in ClockOff?** and
**Show my full morning brief**. Confirm the intended gym, dates and permissions.
Installation and a successful authenticated answer are separate checks.

The grok.com web Plugins screen currently exposes separate connectors and
individual skills. Its previous connector-plus-one-skill setup is not evidence
that this bundled plugin is installed. Keep an existing working connection until
the replacement has been verified.

## Updates and source

This is a generated distribution of the shared ClockOff skills, not an independent
codebase. Version numbers identify package releases; the plugin name stays
**ClockOff**. Staff update the same repository and release a new reviewed ZIP.
Import/update through the host's supported controls; automatic Git updates are
not assumed. No executable hooks, local server, bundled keys or customer data.
The MCP backend remains hosted by ClockOff; GitHub hosts the installable package.

Draft member messages remain unsent. Campaign planning stops for the owner's
review; installing the plugin does not authorize customer sends or spending.

## References

- [Agent Plugins compatible clients](https://agent-plugins.org/compatible-clients)
- [Portable package format](https://agent-plugins.org/plugin-authors/build-an-agent-plugin)
- [Grok Bot packaged skills](https://docs.x.ai/grok-bot/skills-routines-and-automations)
- [Grok Build plugin directories](https://docs.x.ai/build/features/skills-plugins-marketplaces)
