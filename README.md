# Influencer audience check by Followproof

**Influencer audit and influencer vetting from Claude: check audience quality and engagement rate for Instagram, TikTok and YouTube creators, compare finalists and find new ones by niche, through your [Followproof](https://followproof.com) account.**

The plugin connects Claude to the Followproof remote MCP server and adds a skill on how to read the results: lead with the grade, name the signals, and only quote a fake-follower share when Followproof gives one.

[Website](https://followproof.com) · [MCP & API docs](https://followproof.com/developers/) · [Method](https://followproof.com/method/)

## What's inside

| File | Purpose |
| --- | --- |
| [`.mcp.json`](.mcp.json) | Remote MCP server `https://followproof.com/mcp` (Streamable HTTP, OAuth 2.1 with dynamic client registration and PKCE) |
| [`skills/followproof/SKILL.md`](skills/followproof/SKILL.md) | Tools, allowances and how to present results |
| [`.claude-plugin/plugin.json`](.claude-plugin/plugin.json) | Plugin manifest |

## Install

In Claude Code:

```sh
/plugin install followproof --marketplace followproof/plugin
```

Or add the connector only: **Settings → Connectors → Add custom connector** with `https://followproof.com/mcp`. On first use you sign in to Followproof (Google or an email code; new accounts are free) and approve access.

## What you can ask

- "Is @creator's TikTok audience real?"
- "Compare these three Instagram creators for a skincare campaign."
- "Find home-espresso creators on YouTube with 20K–200K subscribers in the US."
- "What should I offer this creator for one sponsored Reel?"
- "Save the two best ones to my Q1 shortlist."

## Tools

`get_account`, `check_creator`, `get_creator_report`, `compare_creators`, `search_creators`, `list_lists`, `get_list`, `create_list`, `add_to_list`, `remove_from_list`. Checks, reports and searches run on your Followproof account and use the same allowance as the web app (free account: 3 full reports, 2 searches and 10 quick checks, one time, no card; Starter and Pro: a fresh allowance every month).

## Privacy

[followproof.com/privacy](https://followproof.com/privacy/). Followproof reads public profile data only; it never posts or messages anyone.
