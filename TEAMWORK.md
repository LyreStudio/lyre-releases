# Build together in Lyre

Lyre brings your team's agent conversations, project work and running apps into
one workflow. Give collaborators access to the projects they need, divide the
work into clear tasks, and review the result together from connected devices.

This guide covers development collaboration and sharing an app with testers.
Controls depend on the installed host and client versions. Start with the
[installation guide](INSTALL.md) and check the
[release notes](https://github.com/LyreStudio/lyre-releases/releases) when a
control described here is unavailable.

## Choose the right access

The computer running a project is its **host**. Each host approves its own
connections and project access. Being on the same network or joining an app team
does not grant development access.

| Access | Who it is for | What it allows |
| --- | --- | --- |
| **Owner** | You or someone you trust to manage the computer through Lyre | Full Lyre host access, including settings and access management. |
| **Developer** | A collaborator working on selected projects | The approved projects' supported agent, source and configured app-service operations. It is not general host administration or unrestricted terminal access. |
| **User / Viewer** | Someone trying an app | Interaction with the explicitly shared app, without access to source, agent conversations, terminals or host settings. |

Developer project selection controls Lyre's project, source and session access.
Agent commands still execute with the host account's operating system permissions.
Approve developers you trust with that execution access. Native desktop control
is a separate capability available to developer connections on supporting builds;
it can expose the whole screen, rather than only a project's files. App viewers
do not receive desktop access.

### Invite a developer

1. On the host, open **Pair Device** or **Manage devices and apps**.
2. Choose **Add a device**, then **Developer**.
3. Name the device or collaborator, select the registered projects they need,
   and review the host execution disclosure.
4. Create the invitation and send the supplied link or invitation to that person.
   They accept it through the connection flow supported by their client.
5. Have them select the same host, project and workspace before starting work.

Developer invitations are single use and have a five minute redemption window.
That window is the time to accept the invitation, not the lifetime of granted
access. Review and revoke saved grants from the host's access list. If Developer
is unavailable, check the host version and registered projects before using a
broader role.

## See the work already in progress

Open the relevant project's workspace and agent conversation to read the request,
the agent's response and the work it has already attempted. Authorized developers
can access ordinary agent conversations within their approved projects. Choose
the same host and conversation to follow the same session; a separate chat has
its own context.

When several devices queue requests for an agent, the shared pending queue shows
the originating device label. Check those requests before sending another task
so you can spot work that is already waiting. Queue controls and attachment
support vary by host version. A device label is display information, not verified
personal authorship for every message.

Some conversations have narrower access. In particular, a remote model conversation
can be private to the developer who opened it. Project access does not override
that restriction.

### Respond to an agent's work

Continue an accessible conversation with a question, correction or next step.
For a specific response, use its copy control and include the relevant passage
in your message. Sending feedback to an agent can start more work; it is not a
passive note visible only to teammates.

For code feedback, the **Changes** view supports inline review comments on diff
lines. On connections with that review workflow, add your comments, return to
the agent composer and check the review attachment before sending. Review drafts
stay on the device until submitted. Restricted developer connections may not
support the full diff or review attachment flow; use a text follow up or ask the
host owner to perform that review.

These are conversation follow ups and code review comments. There is no separate
team comment thread attached to every AI message in the workflow described here.

## Split the work before starting agents

Give each task an outcome, a responsible person or agent, an area to change and
a check that will show it is finished. For example:

| Task | Responsibility | Review evidence |
| --- | --- | --- |
| Improve the checkout layout | One developer and a UI agent | Try the page at desktop and phone sizes. |
| Add checkout validation tests | Another developer and a testing agent | Review the tests and their results. |
| Integrate the changes | The person responsible for the final branch | Review both diffs and test the combined app. |

Use separate agent conversations for independent tasks. Give each agent the
context it needs; opening another conversation does not automatically copy all
other conversations into its prompt. Review existing conversations and pending
requests before assigning more work. Lyre makes work visible, but task ownership
still needs to be agreed by the team.

### Choose a shared workspace or separate worktrees

In one workspace, people and agents use the same checkout. This is useful for
reviewing a shared result or handling carefully separated changes. It also means
overlapping edits can affect each other immediately.

For independent code changes, have the host owner create a **New workspace** with
**New worktree** isolation, or use the project's **New worktree** action where
available. A Git worktree gives a task a separate checkout and branch. It needs
its own applicable setup, dependencies and preview configuration.

Worktrees separate uncommitted edits. The team still reviews, merges and resolves
conflicts when bringing branches together. A separate conversation alone does not
create an isolated checkout, and connecting another computer does not automatically
synchronize its repository with the first one.

## Coordinate agents across computers

On a supporting build, open **Orchestrate** from the agent composer's task mode
control. **On this computer** uses helpers on the selected host. **Across
computers** lets you choose a coordinator and connected target computers, their
workspaces and available models.

Use **Plan and split work** when you want different assignments. Review the plan
before starting it and check which workspace each worker will use. **Same task
everywhere** sends the same task to each selected computer, which is useful for
independent comparisons rather than dividing a job into different parts. Selecting
several models on one computer can also give each model the same assignment, so
check for overlapping writes before dispatch.

Each target host retains its own permissions and must be reachable. Inspect the
per-worker results after dispatch, including any partial failures. Agents already
started have their own lifecycles; closing the planning sheet does not stop them.

Cloud and local models can take different responsibilities. Choose from the models
actually configured and supported by each agent and host. A powerful computer can
run a supported local model while you direct its work from another device. Hardware,
model capability and host availability determine what that setup can do.

## Validate together and invite testers

Have someone other than the task's implementer review the changed files and test
results. The host owner can use **Changes**, the project's terminal and Git
workflow to inspect and integrate the result. Test the combined branch as well as
each individual change.

Use **Open app** to try the actual running app. Check the important actions on
the devices people will use, then bring specific feedback into the agent
conversation. A completed agent turn or a running process is not proof that a
test passed.

Use **Share app** with Viewer access for someone who only needs to try the app.
Where **Teams** is available in access management, it groups app viewers around
selected shared apps and provides membership controls. It is not a developer
group or a grant to read the team's code and conversations. Manage developer
project grants separately.

The host must stay awake, connected and running Lyre. Remote live app previews
require the applicable Pro entitlement; developer connection access and preview
access are separate. See [plans](https://lyrestudio.net/#pricing) and
[connection guidance](https://lyrestudio.net/docs/pairing.html).

## When something is missing

| What you see | What to check |
| --- | --- |
| A teammate cannot see a project or conversation | Confirm the selected host, current project grant and conversation scope. App viewers do not have development access. |
| A worktree has different files or an older result | Check its branch, commits and preview command. Merge the intended changes before testing the combined result. |
| A queue or review action is unavailable | Read the displayed reason and check both host and client versions. Preserve the draft before changing connections. |
| Two agents are changing the same files | Agree on one writer, stop or redirect the overlapping task, or move independent work into separate worktrees. |
| A phone cannot connect or open the preview | Check the host's power, network, running app, current grant and remote preview entitlement. |

[Back to Lyre Studio](README.md) ·
[Report a problem](https://github.com/LyreStudio/lyre-releases/issues/new?template=bug_report.yml)
