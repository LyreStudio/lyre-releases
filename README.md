<p align="center">
  <a href="https://lyrestudio.net"><img src="assets/lyre-mark.png" alt="Lyre Studio" width="64" height="64"></a>
</p>

<h1 align="center">Lyre Studio</h1>

<p align="center"><strong>Build locally. Take it with you.</strong></p>

<p align="center">Your coding agents, your models, your running app.<br>One workspace on your computer. A development loop you can carry across devices.</p>

<p align="center">
  <a href="https://github.com/LyreStudio/lyre-releases/releases/latest"><strong>Download Lyre Studio →</strong></a> ·
  <a href="https://lyrestudio.net/docs/quickstart.html">Get started</a> ·
  <a href="https://lyrestudio.net">Website</a>
</p>

<p align="center">
  <a href="https://github.com/LyreStudio/lyre-releases/releases/latest"><img src="https://img.shields.io/github/v/release/LyreStudio/lyre-releases?style=flat&label=latest&color=4378b5" alt="Latest Lyre Studio release"></a><br>
  <sub>macOS · Windows · Linux · Early access</sub>
</p>

<p align="center">
  <img src="assets/lyre-hero.png" alt="Lyre Studio 0.1.4 on a desktop and iPhone: an agent changes the Harbor Kitchen sample website while the desktop shows the running app" width="100%">
  <br><sub>Real desktop and iPhone captures. Mobile clients are in testing.</sub>
</p>

## From a change to an app you can try

Lyre brings coding agents, project files, terminals, Git review, and interactive
app previews into one workspace. Work on an existing repository or start a new
project. Ask for a change, inspect what changed, and try the result while your
project runs on the computer you chose.

Connect a supported client to continue the conversation or use the app from another
screen. Your host runs the projects and agents; it must stay awake and connected.

## Get Lyre Studio

[**Download the latest release →**](https://github.com/LyreStudio/lyre-releases/releases/latest)

| Your computer | Recommended download | Availability |
| --- | --- | --- |
| **macOS · Apple silicon** | **.dmg** — open, then drag Lyre to Applications | 0.1.4 is signed and notarized |
| **Windows · Intel / AMD 64-bit** | **Setup .exe** installer | Available · unsigned |
| **Linux · Intel / AMD 64-bit** | **AppImage**, or **.deb / .rpm** | Available · unsigned |

No Intel Mac package is currently published. iOS and Android clients have separate
testing and distribution channels; check [mobile availability](https://lyrestudio.net/docs/release-status.html#ios).

[Installation and updates](INSTALL.md) · [Release notes](https://github.com/LyreStudio/lyre-releases/releases) ·
[Compare plans](https://lyrestudio.net/#pricing)

## Keep your tools. Choose your models.

**Work where your code already lives.** Bring your repositories, development
services, terminals, and Git workflows. Local projects and local-network workflows
work without a Lyre cloud account. Your project's own tools and dependencies still
run on the host.

**Choose the agent for the task.** Lyre supports Claude, Codex, OpenCode, Pi, and
other provider integrations. Keep conversations organized by project, run independent
work in separate worktrees, and review the results together. Provider accounts,
installation requirements, and model access vary.

**Use local models alongside cloud providers.** Connect Ollama, LM Studio,
llama.cpp, or a compatible model server. Choose the models you want to use and
follow the supported setup flow. Local inference depends on your hardware and
chosen agent's model support.

<p align="center">
  <img src="assets/model-choice.png" alt="Lyre Studio 0.1.4 Connections screen showing model-source choices and setup actions" width="100%">
</p>

## See the change. Try the result.

**Your agent and app, together.** Keep a live preview beside the conversation,
or open the app on its own. Agent work and app previews have independent lifecycles.

**Review before you ship.** Inspect file changes and diffs, use your project's
tests, and read terminal output. A running app is something you can try; your
checks determine whether the change is ready.

**Bring feedback into the next turn.** Attach a preview screenshot to the agent
conversation. Explicitly send bounded diagnostics or client error reports to an
agent authorized for that project.

<p align="center">
  <img src="assets/review-changes.png" alt="Lyre Studio 0.1.4 Changes view showing the actual diff for a sample website edit" width="100%">
</p>

## Carry the development loop across devices

Continue agent work on a connected client, try a website by touch, or play the
browser game you are building. Lyre keeps computer and project context visible
so you know where the work is running.

<p align="center">
  <img src="assets/phone-agent.png" alt="Reviewing an agent's completed change on iPhone" width="30%">&nbsp;
  <img src="assets/phone-preview.png" alt="Trying the Harbor Kitchen sample website in Lyre on iPhone" width="30%">&nbsp;
  <img src="assets/phone-game.png" alt="Playing the Orbit Run sample browser game in Lyre on iPhone" width="30%">
  <br><sub>Direct the work. Try the website. Play the game.<br>Earlier testing-build captures; these demonstrate the workflow, not every platform's current release.</sub>
</p>

**Give testers access to the app.** App-only sharing grants access to an explicitly
shared app, with revocation controls. It keeps source files, agent sessions,
terminals, and host settings outside that viewer's access. Client-preview support
varies by platform and build. Pro includes remote live app previews and app-scoped
sharing; see [plans](https://lyrestudio.net/#pricing).

<details>
<summary><strong>More of the workspace: automation, routing, publishing, and customization</strong></summary>

- **Activity and schedules:** see work that needs input, is ready to review, or is
  still running; configure recurring agent tasks and notifications.
- **Model routing:** manage model sources, catalogs, routes, and usage through the
  supported routing integrations. Runtime availability varies by platform.
- **Release tools:** prepare mobile publishing with integrated Fastlane tools
  and your configured signing, platform tooling, and store accounts. Setup is
  separate from a completed store submission.
- **Marketplace and plugins:** browse project starters and templates, and manage
  executable host plugins. Community Extensions are a discovery catalog;
  extension installation is unavailable.
- **Guided or Developer:** choose a simpler project-to-chat-to-preview flow or a
  denser development workspace, while retaining selected work and drafts.
- **Remote desktop:** 0.1.4 includes native desktop-viewing and control surfaces.
  Installed cross-device qualification remains in progress; support depends on
  host permissions, platform, and build. App-only sharing does not grant desktop access.

Lyre is in early access. Capabilities depend on the installed build, provider,
platform, and configured services. Release notes describe version-specific changes
and known limitations.

</details>

## Your first development loop

1. **Open a project.** Choose the folder on the computer that will run it.
2. **Connect an agent or model.** Follow its installation and account setup.
3. **Make a change and try it.** Configure the preview command, run the app, and
   review the agent's work.
4. **Connect another device.** Use **Pair Device** with a supported client and
   explicitly grant the access it needs.

[First-project guide](https://lyrestudio.net/docs/quickstart.html) ·
[Existing projects](https://lyrestudio.net/docs/projects.html) ·
[App recipes](https://lyrestudio.net/docs/app-recipes.html)

## Help shape Lyre

[Report a bug](https://github.com/LyreStudio/lyre-releases/issues/new?template=bug_report.yml) ·
[Request a feature](https://github.com/LyreStudio/lyre-releases/issues/new?template=feature_request.yml) ·
[Join Discord](https://discord.gg/eGjaBGJgp) ·
[Read the docs](https://lyrestudio.net/docs/index.html)

For security issues, use [private reporting](SECURITY.md).

---

This is Lyre Studio's official repository for **downloads, release notes, and
feedback**. Application source is maintained privately. **Lyre Studio is proprietary**;
see the [license notice](LICENSE), [EULA](https://lyrestudio.net/legal/eula.txt), and
[third-party licenses](https://lyrestudio.net/legal/third-party-licenses.html).
The application foundation derives from [Paseo](https://github.com/getpaseo/paseo),
with its Apache-2.0 license and notices preserved.

<p align="center"><sub>© 2026 Jonathan Bakhit · Lyre Studio · <a href="https://lyrestudio.net/privacy.html">Privacy</a></sub></p>
