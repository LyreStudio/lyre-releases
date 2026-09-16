# Lyre Studio

**Build your idea. Try it on your phone.**

Run coding agents, follow the work, and test local apps on real devices from one private,
local-first development workspace. Your source, tools, and environment stay on your own
computer.

![Lyre desktop workspace](https://lyrestudio.net/lyre-desktop-workflow-v2-1536.webp)

Downloads for Windows, macOS, and Linux live in this repository's
[Releases](../../releases).

---

## What it is

Lyre is a desktop host plus mobile and desktop clients. The desktop companion starts and
manages your project; the phone (or another computer) acts as a client for launching,
testing, editing, and steering agents. Nothing about your development environment moves to
somebody else's cloud.

- **Same features as Paseo, plus more** — multi-provider agent control, phone previews,
  teams, managed AI, and voice input in one workspace.
- **Local-first** — your computer runs the project. You can point Lyre at a project folder
  you already have.

## Why

Development tooling drifted into two bad shapes: agents that live only on one machine, and
"cloud workspaces" that move your whole environment off your desk. Lyre keeps the power of
the second without the cost of the first — remote access to *your* machine, not a copy of
your project on someone else's.

---

## Agents

**Give every task the right pair of hands.** Run multiple coding agents at once, mix
supported providers, and hand work between them for implementation, review, or a second
opinion.

Supported providers: Claude Code · Codex · Copilot · OpenCode · Pi · Lyre AI, plus custom
providers and local models.

**Move faster without agents colliding.** Give separate agents their own Git worktrees so
implementation, investigation, and review can happen at the same time without overwriting
the same working copy.

## Preview on real devices

**From local code to a real phone.** Pair Lyre once, choose an app, and let the desktop
start its configured services. Test the live project on your phone without creating a
separate mobile build for every change.

**Open the app, not a setup checklist.** Lyre starts the configured frontend and supporting
services, waits until they are healthy, and opens the preview. When something fails, the
useful output is already there.

![Phone preview](https://lyrestudio.net/harbor-phone-app-v2-768.webp)

## Remote access — local-first

**Cloud-like access. Your machine stays the host.** Connect directly on your network, or
securely through Lyre's encrypted relay when you are away. Each host resolves whether to
connect locally or remotely on its own, so a machine on your desk and one across the
country can both be in your list.

- Remote connections, code editing, agent conversations, and project startup are **free**.
- **Pro** is required only for **live app previews outside your local network**. Previewing
  on your local network stays free.
- AI provider charges are separate.

## Teams

**A shared view of the work.** Follow active agent sessions, prompts, progress, and changed
files from one workspace. Teammates can see what is moving before they start something new.

**Share the app, not your whole workspace.** Invite people to specific apps with revocable,
app-scoped access — *User mode*. They can use the app while source, terminals, agents, and
host controls stay behind the developer boundary. Invite a single person or a whole team,
with expiring links and QR pairing, and kick or ban a device if you need to.

## Building

- **Files and search** — browse the project, then search filenames or file contents with
  case, whole-word, and regex options and a scope picker.
- **Terminal** — run commands and watch output, with your own terminal profiles.
- **Changes** — review diffs and commit history for the working copy.
- **Browser and app viewer** — open web targets and app previews as independent panels.

## Managed AI and voice

**Lyre AI** is a managed option for people who do not want to pick a provider, buy credits,
or manage keys. Subscribe to the Lyre AI plan and it appears in your provider list already
selected — no setup. It runs alongside bring-your-own providers; they are not replaced.

**Voice input** is included on every plan: five minutes per day on Free, no usage quota on
Pro. One recording may be up to two minutes. The daily allowance resets at 00:00 UTC.

---

## Platforms

| Platform | Role |
| --- | --- |
| **Desktop host** | Runs your project, services, agents, and the relay connection |
| **Phone client** | Launch, preview, edit, and steer from iOS or Android |
| **Desktop client** | The same workspace on a second computer |

Your host computer runs the project, so it needs to stay awake and online while you use a
connected screen.

## Plans

| | **Free** | **Pro** | **Lyre AI** |
| --- | --- | --- | --- |
| Local projects and paired devices | Yes | Yes | Yes |
| Remote connections, chat, and screenshots | Yes | Yes | Yes |
| Live app previews on your local network | Yes | Yes | Yes |
| Live app previews outside your network | — | Yes | Yes |
| Voice input | 5 min/day | No quota | No quota |
| Concurrent client limit | 3 | 10 | 25 |
| Paired devices | 20 | 20 | 100 |
| Hosts per account | 1 | 1 | 3 |
| Managed **Lyre AI** access | — | — | Included |

Team features and app-scoped invitations are available on paid plans. Prices and checkout
are on [lyrestudio.net](https://lyrestudio.net).

## Architecture at a glance

- **Host** — a local daemon on your computer manages projects, services, agent processes,
  and remote access.
- **Clients** — desktop and mobile clients talk to the host directly on your network, or
  through Lyre's encrypted relay when you are away.
- **Relay** — carries encrypted traffic; media uses a WebRTC relay (Cloudflare Realtime) for
  remote streams, with a direct/WebSocket fallback.
- **Preview** — the host starts your configured services, checks readiness, and streams the
  app viewport to the client's viewer.
- **Providers** — each agent provider is an adapter behind one interface, so provider choice
  stays a setting rather than a fork.
- **Extensions** — MCP servers, plugins, and marketplace entries extend the workspace;
  extensions never replace the host as the security boundary.

## Status and limits

- Development builds are unsigned on Windows, so expect SmartScreen warnings on install.
- Live app previews outside your network require the host to be awake, online, and running
  Lyre; your existing app permissions still apply.
- Lyre works with supported websites, web apps, and browser-based tools, including React,
  Vite, Next.js, Expo web, and Capacitor projects. Open an existing project folder and keep
  working with its files.
- Some capabilities below are planned rather than shipped.

**Coming soon:** select UI elements for targeted edits · visual controls for layout,
typography, and styling · remote host wake · host and app restoration across devices · agent
screenshots, recordings, logs, tests, and diffs · agent tasks from issues, pull requests,
and team messages · reusable project blueprints · guided builds and store releases.

## Documentation and community

- Site and docs — [lyrestudio.net](https://lyrestudio.net) · [docs](https://lyrestudio.net/docs/index.html)
- Quick start — [your first project](https://lyrestudio.net/docs/quickstart.html)
- Extend it — [create plugins & integrations](https://lyrestudio.net/docs/create-plugin.html)
- Account — [delete your account](https://lyrestudio.net/docs/account-deletion.html)
- Community — [Discord](https://discord.gg/ZRrY5DtZk)
- Privacy — [privacy policy](https://lyrestudio.net/privacy.html)

## Getting the app

Download the installer for your platform from [Releases](../../releases). Install the
desktop host first, then pair your phone from the app.

---

© 2026 Lyre. Third-party licenses are listed in the app and on the
[licenses page](https://lyrestudio.net/legal/third-party-licenses.html).
