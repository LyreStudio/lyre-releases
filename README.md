<p align="center">
  <a href="https://lyrestudio.net"><img src="assets/lyre-mark.png" alt="Lyre Studio" width="64" height="64"></a>
</p>

<h1 align="center">Lyre Studio</h1>

<p align="center"><strong>Build locally. Take it with you.</strong></p>

<p align="center">Build, test, and preview apps with coding agents and local models, then take your workspace across devices.</p>

<p align="center">
  <a href="https://github.com/LyreStudio/lyre-releases/releases/latest"><strong>Download Latest Release</strong></a> ·
  <a href="https://lyrestudio.net">Website</a> ·
  <a href="https://lyrestudio.net/docs/index.html">Documentation</a>
</p>

<p align="center">
  <a href="https://github.com/LyreStudio/lyre-releases/releases/latest"><img src="https://img.shields.io/github/v/release/LyreStudio/lyre-releases?style=flat&label=latest&color=4378b5" alt="Latest Lyre release"></a><br>
  <sub>Windows &amp; Linux desktop · Early access · <a href="INSTALL.md#macos">macOS preview status</a></sub>
</p>

<p align="center">
  <img src="assets/desktop-studio.png" alt="Lyre Studio showing a coding agent and the running Harbor Kitchen sample app side by side" width="100%">
  <br><sub>Your agent and your working app, together. Actual Lyre interface with a sample project.</sub>
</p>

## Download and install

[**Get the latest release →**](https://github.com/LyreStudio/lyre-releases/releases/latest)

| Your computer                     | Choose this download                                       |
| --------------------------------- | ---------------------------------------------------------- |
| **Windows** · 64-bit Intel or AMD | **Setup .exe** installer                                   |
| **Linux** · 64-bit Intel or AMD   | **AppImage**, or **.deb** / **.rpm** for your distribution |

1. Open the latest release and choose the download for your computer.
2. Run the Windows installer, or install/open your Linux package.
3. Launch Lyre Studio and open a project folder.

Windows builds are currently unsigned and may show a SmartScreen warning.
[Installation, macOS status, and updates](INSTALL.md) ·
[What's changed](https://github.com/LyreStudio/lyre-releases/releases)

## Built around your development environment

**Local projects. Local models. Your tools.** Work with your existing repositories,
terminals, services, and Git workflows. Connect **Ollama, LM Studio, llama.cpp**, or a
compatible model server alongside your chosen cloud providers. Local projects and
local-network workflows work without a Lyre cloud account.

**Orchestration across models and devices.** Use supported coding agents in parallel,
with separate worktrees for independent tasks. [Paseo](https://github.com/getpaseo/paseo)
powers the agent sessions and host connections. Lyre brings those sessions together
with your projects, local-model setup, and interactive app previews.

**Model routing built in.** The [OmniRoute](https://github.com/diegosouzapw/OmniRoute)
integration connects your gateway's model catalog to Lyre's agent workflow. Choose
models and use your gateway's configured routing and fallbacks from one workspace.

**Test the result as you build.** Review diffs, run your project's tests, inspect
terminal output, and interact with the live app beside the agent. Try a change on
another device and bring what you find straight back into the conversation.

**Carry the release workflow through.** Integrated
[Fastlane](https://github.com/fastlane/fastlane) tools bring signing, screenshots,
TestFlight, and Android publishing into the project workflow, using your configured
platform tools and store accounts. Desktop and custom projects can use their own
publishing setup.

## Take your apps with you

A website, dashboard, personal tool, or browser game: open the real app running on
your computer from a paired device. Steer an agent, try the result, and keep improving
it from the screen in your hand.

<p align="center">
  <img src="assets/phone-agent.png" alt="Reviewing an agent's completed change on iPhone" width="30%">&nbsp;
  <img src="assets/phone-preview.png" alt="Using the Harbor Kitchen sample website in Lyre's iPhone preview" width="30%">&nbsp;
  <img src="assets/phone-game.png" alt="Playing the Orbit Run sample browser game in Lyre on iPhone" width="30%">
  <br><sub>Direct the work. Try the website. Play the game. Actual iPhone testing-build captures.</sub>
</p>

Your host runs the project and stays awake while you connect locally or remotely.
Pro adds live app previews outside your local network and app-scoped sharing.
[Compare plans](https://lyrestudio.net/#pricing).

Lyre is in early access; features depend on your installed build. iOS and Android
clients are in testing. Follow [mobile availability](https://lyrestudio.net/docs/release-status.html#ios)
for distribution updates.

## Start building

Open a project, choose your coding provider or local model, and configure the app's
preview command. Run the app, give your agent a task, and validate the result.
Use **Pair Device** to connect another supported client to your host.

[First-project guide](https://lyrestudio.net/docs/quickstart.html) ·
[Connect an existing project](https://lyrestudio.net/docs/projects.html) ·
[App recipes](https://lyrestudio.net/docs/app-recipes.html)

## Help and releases

- **Something broke?** [Report a bug](https://github.com/LyreStudio/lyre-releases/issues/new?template=bug_report.yml).
- **Have an idea?** [Request a feature](https://github.com/LyreStudio/lyre-releases/issues/new?template=feature_request.yml).
- **Need a hand?** Join the [Discord community](https://discord.gg/ZRrY5DtZk) or read the [documentation](https://lyrestudio.net/docs/index.html).
- **Following updates?** Browse [release notes and previous downloads](https://github.com/LyreStudio/lyre-releases/releases).
- **Found a security issue?** [Report it privately](SECURITY.md).

This is Lyre Studio's official public hub for downloads, release notes, and feedback.
**Lyre Studio is proprietary and is not currently open source.** Application source
is maintained privately. Use of the app is governed by the
[End User License Agreement](https://lyrestudio.net/legal/eula.txt); see the
[license notice](LICENSE) and [third-party licenses](https://lyrestudio.net/legal/third-party-licenses.html).

<p align="center"><sub>© 2026 Jonathan Bakhit · Lyre Studio · <a href="https://lyrestudio.net/privacy.html">Privacy</a></sub></p>
