# Google Summer of Code 2026 [Rocket.Chat]

<div align="center">
 <a href=""><img src="https://github.com/user-attachments/assets/76884849-7bf1-4ec7-b3bf-197dfa2b270f" width="720" alt="google-summer-of-code" style="background-color: black;"></a>
</div>

# EmbeddedChat & Rocket.Chat Apps — My work

## Introduction

I contribute to [EmbeddedChat](https://github.com/RocketChat/EmbeddedChat), a lightweight embeddable chat client that talks to a Rocket.Chat server over REST and real-time APIs. My focus is on **chat UX**, **message flows**, **media/attachments**, and **Rocket.Chat Apps (UI Kit + slash commands)** so embedded experiences stay close to full Rocket.Chat behaviour.

## What I worked on

### EmbeddedChat (UI & behaviour)

- **Quoted message UX** — Opening the user profile from quoted content: composer quote preview and inline quote blocks now open the same **User Information** sidebar as normal message avatars when clicking the quoted author avatar or username.
- **Bulk message selection** — Multi-select mode from the message toolbox (`Select message`), checkboxes on messages, bottom action bar with **Select all / Deselect all**, **Cancel**, and **Delete**, with permission-aware deletes and confirmation.
- **Reactions** — Emoji picker path now **toggles** an existing reaction (same behaviour as clicking the reaction on the message).
- **Audio / attachments** — Improvements around preview, authenticated media URLs where needed, and download naming so audio flows behave more predictably in embedded + Storybook setups.
- **UI polish** — Tooltip / DOM nesting fixes where inline markup met block-level wrappers.

*Replace this list with your exact PR links once merged — see table below.*

### Rocket.Chat Apps (private / custom)

I built and deployed **three** Rocket.Chat Apps on my workspace:

| App | Purpose (short) |
|-----|------------------|
| **Poll** | Create and run polls (e.g. via slash command / UI Kit flow). |
| **Grammar check** | Check or improve message text from chat. |
| **Activity** | Surface per-user or workspace activity insights. |

These apps use the standard **Apps-Engine** workflow (`rc-apps create`, deploy/package) and integrate with Rocket.Chat’s **UI Kit** where modals or contextual views are needed. Reference: [Create an App](https://developer.rocket.chat/docs/create-an-app).

### How this connects to EmbeddedChat

EmbeddedChat already supports **UI Kit interactions** (`/api/apps/ui.interaction/:appId`) and renders **modals / contextual bars** from app responses. My apps are designed to be triggered the same way as in the main Rocket.Chat client (slash commands, and optionally future toolbar actions in the composer).

## Showcase

<!-- Add screenshots or short screen recordings -->

- Quoted message → profile sidebar from avatar/username  
- Bulk select → delete flow  
- Poll / grammar / activity app demos (RC web + EmbeddedChat if wired)

## Contributions (PRs)

| PR | Title |
|----|--------|
| <!-- #123 --> | <!-- Short title + link --> |
| <!-- #124 --> | <!-- ... --> |

[All my EmbeddedChat PRs](https://github.com/RocketChat/EmbeddedChat/pulls?q=is%3Apr+author%3AYOUR_GITHUB_USERNAME)

## Tech stack touched

- `packages/react` — Message list, quote UI, attachments, toolbox, stores  
- `packages/api` / auth flows — Where relevant for media or commands  
- `packages/ui-elements` — Small shared UI fixes (e.g. tooltip)  
- **Rocket.Chat Apps** — TypeScript, Apps-Engine, UI Kit

## Learn more

- [EmbeddedChat docs](https://rocketchat.github.io/EmbeddedChat/)  
- [Create a Rocket.Chat App](https://developer.rocket.chat/docs/create-an-app)

## Connect

| | |
|--|--|
| **Name** | YOUR NAME |
| **GitHub** | [@YOUR_USERNAME](https://github.com/YOUR_USERNAME) |
| **LinkedIn** | YOUR_LINK |
| **Email** | YOUR_EMAIL |

## Acknowledgements

Thanks to the EmbeddedChat maintainers and the Rocket.Chat community for reviews and guidance.

---

*This README describes my contributions only. It is not affiliated with Google Summer of Code unless you explicitly participated — add a GSoC banner and program link if applicable.*
