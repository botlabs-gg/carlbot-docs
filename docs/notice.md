# Transitioning to Slash Commands

!> **Notice:** Carl-bot is officially phasing out traditional prefix commands (e.g., `!ban`, `?kick`). We are moving exclusively to Discord's native Slash Commands (`/`).

## Why the change?

Discord is shifting toward Slash Commands to improve user privacy, security, and discoverability. We need to align with Discord's requirements for privileged Intents, and Slash Commands are slowly becoming a requirement for bots to function properly in the future.

## Timeline

- **Currently:** Prefix commands still function but will sometimes trigger a warning message.
- **5th October 2026:** Standard prefix commands will be fully disabled.

## How to Prepare Your Server

Making the switch is easy, but you need to ensure your server permissions are set up correctly:

1. **Start using `/`:** Simply type `/` in any channel to pull up the command menu and select Carl-bot.
2. **Enable Permissions:** Ensure that Carl-bot (and your server members) have the **Use Application Commands** permission enabled in your Server Settings > Roles.
3. **Update Integrations:** If you have any external integrations or server guides instructing users to use prefix commands, update those texts to reflect the new slash commands.

## Frequently Asked Questions

**Will my Tags stop working?**
No, Tags will continue to work as normal. There will be no changes to Tags and how they function.

**Will the mention commands stop working too?**
No, mention commands (e.g., `@Carl-bot ban`) will continue to work as normal. You can still use them to trigger commands, but we recommend switching to Slash Commands for a better experience.

**I can't see Carl-bot's slash commands. How do I fix this?**
If the commands aren't showing up, make sure you users have the **Use Application Commands** permission enabled. If it's still not working, re-invite Carl-bot using the official invite link on the dashboard to refresh its integration permissions.

?> **Need more help?** Join our [support server.](https://discord.gg/S2ZkBTnd8X) for any further queries regarding this transition.
