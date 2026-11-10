# Earlyfollow skill

Use Earlyfollow from an AI agent with the product's existing authorization and usage rules.

[Website](https://earlyfollow.com/) · [Agent setup](https://earlyfollow.com/docs/agents)

## Install

With Node.js 22.20 or newer and npm available, install the skill using the skills CLI:

```sh
npx skills add earlyfollowhq/skills --skill earlyfollow
```

Select your supported agent and installation scope in the installer. Restart your agent session after installation. This installs instructions; it does not connect MCP, install the product CLI, sign you in or grant access. Follow [Agent setup](https://earlyfollow.com/docs/agents) to connect the product.

Alternatively, use the existing npm installer:

```sh
npx earlyfollow-client skill install --target codex
# Or use --target grok
```

Choose one installer for this skill so two copies do not drift. For CLI usage, install `earlyfollow-client` separately and follow the setup documentation. Credentials belong in your secret store, never in this repository.

## Updates

For an installation managed by the skills CLI, use `npx skills update earlyfollow`. Choose the same project or global scope used during installation. Review any local edits before updating. For the npm installer, rerun its install command; it protects modified files.

## Usage and support

Each successful data call costs 1 credit. Pro includes 10,000 calls a month. Calls stop when the allowance is exhausted. Replays use the original result for 30 days without another charge.

Installing the skill is free. Product calls follow the site's account, authorization and billing rules. For setup and product support, see [the documentation](https://earlyfollow.com/docs/agents).

Skill source version: 0.1.1. MIT licensed; see [LICENSE](LICENSE).
