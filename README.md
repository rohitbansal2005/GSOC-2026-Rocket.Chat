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


### Rocket.Chat Apps (private / custom)

I built and deployed **three** Rocket.Chat Apps on my workspace:

<a>https://github.com/rohitbansal2005/RC-APP</a>

<img width="2854" height="1694" alt="Screenshot 2026-03-28 121042" src="https://github.com/user-attachments/assets/33bf1cc2-c6c4-4177-8282-ea520abf91a8" />



| App | Purpose (short) |
|-----|------------------|
| **Poll** | Create and run polls (e.g. via slash command / UI Kit flow). |
| **Grammar check** | Check or improve message text from chat. |
| **Activity** | Surface per-user or workspace activity insights. |

### Demo Videos (RC Apps)

#### Poll (RC App)


https://github.com/user-attachments/assets/c790132d-abf2-4359-8b90-555d6bdb2f6d

#### GrammarChecker (RC App)



https://github.com/user-attachments/assets/cd8faba6-005d-4805-96e4-9db3fc3705e8

#### Activity (RC App)



https://github.com/user-attachments/assets/c8372920-2bd3-4fe4-a569-85ab35851f56



These apps use the standard **Apps-Engine** workflow (`rc-apps create`, deploy/package) and integrate with Rocket.Chat’s **UI Kit** where modals or contextual views are needed. Reference: [Create an App](https://developer.rocket.chat/docs/create-an-app).

### How this connects to EmbeddedChat

EmbeddedChat already supports **UI Kit interactions** (`/api/apps/ui.interaction/:appId`) and renders **modals / contextual bars** from app responses. My apps are designed to be triggered the same way as in the main Rocket.Chat client (slash commands, and optionally future toolbar actions in the composer).

## Showcase

<!-- Add screenshots or short screen recordings -->

- Quoted message → profile sidebar from avatar/username  
- Bulk select → delete flow  
- Poll / grammar / activity app demos (RC web + EmbeddedChat if wired)

## Contributions

### 🔹 Key Contributions — EmbeddedChat

| Issue | Title | Impact |
|------|------|--------|
| #1251 | User profile sidebar doesn’t open from quoted message | Fixed inconsistency between quoted and normal messages, improving navigation UX |
| #1249 | Multi-message selection & bulk delete | Enables faster moderation and message management |
| #1247 | Audio playback & incorrect file format | Improves reliability of audio messages and attachments |
| #1245 | Emoji reaction inconsistency via picker | Ensures consistent toggle behavior (aligned with Slack/Discord UX) |

👉 View all EmbeddedChat contributions:  
https://github.com/RocketChat/EmbeddedChat/issues?q=author%3Arohitbansal2005

---

### 🔹 Contributions — Rocket.Chat Core

| Issue | Title | Impact |
|------|------|--------|
| #39792 | Make roomId optional in mentioned/starred APIs | Enables global data fetching across rooms |
| #39791 | Activity Hub global fetch for mentions & starred | Supports unified activity dashboard feature |
| #39765 | Cache settings in OmnichannelTranscript | Reduces repeated API/database calls (performance improvement) |
| #39762 | Inconsistent return type in parseUriList | Fixes OAuth redirect handling bug |

👉 View all Rocket.Chat contributions:  
https://github.com/RocketChat/Rocket.Chat/issues?q=author%3Arohitbansal2005


## Contributions

### 🔹 Pull Requests — EmbeddedChat

| PR | Title | Impact |
|----|------|--------|
| #1252 | Open user info sidebar from quoted messages | Fixes UX inconsistency and improves user navigation |
| #1250 | Multi-message selection & bulk delete | Enables efficient moderation and bulk actions |
| #1248 | Fix audio playback & download handling | Improves reliability of audio messages and attachments |
| #1246 | Emoji reaction toggle via picker | Ensures consistent UX (aligned with Slack/Discord behavior) |

👉 View all EmbeddedChat PRs:  
https://github.com/RocketChat/EmbeddedChat/pulls?q=author%3Arohitbansal2005

---

### 🔹 Pull Requests — Rocket.Chat Core

| PR | Title | Impact |
|----|------|--------|
| #39793 | Make roomId optional in mentioned/starred APIs | Enables global activity fetching across rooms |
| #39766 | Cache settings in OmnichannelTranscript | Reduces repeated API calls (performance optimization) |
| #39763 | Normalize parseUriList return type | Fixes OAuth redirect handling bug |
| #39734 | Fix livechat transfer comment overflow | Improves UI rendering for long messages |
| #39705 | Add autocomplete for TOTP fields | Enhances UX with password manager support |

👉 View all Rocket.Chat PRs:  
https://github.com/RocketChat/Rocket.Chat/pulls?q=author%3Arohitbansal2005

---
### 🔹 Contribution Highlights

- Improved chat UX consistency across multiple interaction flows  
- Built scalable features like bulk message actions  
- Optimized backend performance with caching strategies  
- Fixed critical API and authentication-related issues  
- Contributed across multiple repositories in the Rocket.Chat ecosystem  
---
## Tech stack touched

- `packages/react` — Message list, quote UI, attachments, toolbox, stores  
- `packages/api` / auth flows — Where relevant for media or commands  
- `packages/ui-elements` — Small shared UI fixes (e.g. tooltip)  
- **Rocket.Chat Apps** — TypeScript, Apps-Engine, UI Kit
---
## Connect

| **Role**           | **Rohit Kumar Bansal – GSoC Participant**                                      |
| :----------------- | :----------------------------------------------------------------------------- |
| **Affiliation**    | [Rocket.Chat](https://rocket.chat/)                                            |
| **Project**        | EmbeddedChat & Rocket.Chat Contributions                                       |
| **GitHub**         | [@rohitbansal2005](https://github.com/rohitbansal2005)                         |
| **LinkedIn**       | [@rkbansal23](https://linkedin.com/in/rkbansal23)                              |
| **Email**          | [rohitkumarbansal23@gmail.com](mailto:rohitkumarbansal23@gmail.com)            |
| **Rocket.Chat**    | [rohit.kumar.bansal](https://open.rocket.chat/direct/rohit.kumar.bansal)       |

## Acknowledgements

Thanks to the EmbeddedChat maintainers and the Rocket.Chat community for reviews and guidance.

---
