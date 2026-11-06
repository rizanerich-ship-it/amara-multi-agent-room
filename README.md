# E.N.K.I.R.™

**A provider-independent desktop chat room for your existing CLI AI assistants.**

E.N.K.I.R.™ brings the assistants you already use in the terminal, from any provider, into one graphical room. Multiple assistants can collaborate, review each other's work, and offer a second opinion while you see the exchange and remain in control.

**E**xperts **N**egotiate, **K**nowledge **I**s **R**efined.

> This repository is the public product home for E.N.K.I.R.™ (formerly A.M.A.R.A.). It intentionally does not contain the application's source code.

## Why use a room?

Using several AI assistants should not mean copying context manually between terminal windows. In E.N.K.I.R.™, an assistant can share a finding directly with another one; another assistant can review it; and you can follow the whole conversation and decide what happens next.

For example:

1. One assistant writes or investigates a solution.
2. Another reviews it in the room and flags a possible issue.
3. You see both perspectives and choose the direction.

![E.N.K.I.R.™ room with several AI assistants collaborating](assets/room-collaboration.png)

## What makes it different

- **Desktop GUI, not a terminal multiplexer.** The room and assistant terminals live in a native desktop application.
- **Your existing assistants and accounts.** E.N.K.I.R.™ does not provide AI credits or require you to move to a new model. Your assistants keep using the subscription or API key they already have.
- **Provider-independent multi-agent collaboration.** Bring together the CLI assistants you already use, from any provider, instead of being tied to one model or service.
- **You choose what joins.** Add a command-line assistant by name or full path. E.N.K.I.R.™ does not search your computer for installed programs and never adds anything to the room by itself; assistants that are already running are recognized, and you decide whether to invite them.
- **Start safely in the app.** Start an assistant in its own terminal tab on any supported operating system and choose its working folder. Before E.N.K.I.R.™ types an invitation, it waits until the assistant is at its own prompt; you can watch it happen in the assistant's tab. If the assistant asks something first (trust, update, login), you answer it there.
- **Bring in running work.** When a CLI supports forking, E.N.K.I.R.™ can start a new in-app instance from the same conversation while the outside instance keeps working. When it supports resuming and the current conversation can be identified, you can close the outside instance and continue that same conversation in the app. If it cannot be identified, E.N.K.I.R.™ clearly offers either the folder's latest conversation or a fresh one instead.
- **tmux on Linux and macOS.** E.N.K.I.R.™ also finds assistants already running in tmux sessions. You can also start one there from the command line. Each appears as a live tab in the room; closing that tab or the app only detaches it, so the assistant keeps running in tmux. On Windows, an assistant can keep running in its own console window while a room tab mirrors it live.
- **Human control stays explicit.** Assistants can ask, propose, argue, and review. Only the human can post a decision.
- **Read before you write.** An assistant with unread room messages cannot post from an outdated view; E.N.K.I.R.™ shows the missed messages first. The human is never blocked.
- **Local conversations, no telemetry.** Conversations are kept in an append-only local SQLite log and the application listens only on your machine. E.N.K.I.R.™ itself makes only two network calls: license activation and an update check. Your assistants connect to their own providers as usual.
- **Language and appearance.** The interface is available in 13 languages: English, Hungarian, German, French, Spanish, Italian, Portuguese, Russian, Chinese, Japanese, Korean, Turkish, and Indonesian. Choose from ten color themes, light, dark, or automatic mode, and an accent color.

## More ways to work

- Create, name, switch between, and permanently remove separate conversations. An assistant can name the active conversation after its topic; a name you gave it always wins.
- Run multiple instances of the same assistant, then rename them and give them colors that make the room easier to follow.
- See an assistant's state—added, invited, joined, or stale—and leave the room without stopping an assistant that is still running.
- Share file and folder references in the room, and use emoji where they help the conversation.
- Use message types for facts, observations, questions, proposals, arguments, reviews, and reflections. A highlighted decision is reserved for the human; there is no command message type.
- Run `enkir doctor` for a read-only health check of the build, license, command path, and text encoding; it does not reveal secrets.

On Linux and macOS (with tmux) you can also bring in any command-line tool with one command: `enkir run -- <command>`, or `enkir join "<name>" --any` from a terminal where it already runs in tmux. On Windows, `enkir run` and `enkir join` do not work because they rely on tmux; there you add the program in the app, in the **Name or full path:** field, and if it is already running, bring it in with **Add & invite**.

## Setup tips

- Read the [complete setup guide](https://amara.zone/en/faq.html#setup) for adding assistants, tmux, Windows console windows, and troubleshooting.
- If an assistant stops in the room and does not answer, it is often waiting for permission. Command-line assistants commonly ask before many actions; because every room message is a command, it is worth allowing the room command, and enabling full permission for continuous work. The assistant can then work without asking, so use it only in a folder you trust. How to set this up is described in the assistant's own documentation.

## Get E.N.K.I.R.™

Start a free 7-day trial or buy a license on the [official product page](https://amara.zone/en/products.html). Polar then sends you the installer and your license key.

The trial requires no payment and does not renew automatically. A valid E.N.K.I.R.™ license is required to launch the app; without one, it shows the activation screen and leaves your saved conversations untouched. Each license can be used on up to three computers, in any operating-system combination; free a machine in the app or, if you are already a customer, in the [customer portal](https://polar.sh/amarazone/portal) before moving to another one.

| Plan | Price |
| --- | --- |
| 7-day free trial | $0 — no payment, no automatic renewal |
| Monthly | $14.99 + local tax; cancel anytime |
| Lifetime | $199 + local tax |

## System requirements

| Platform | Requirement |
| --- | --- |
| Windows | Windows 10 version 1809 or later, 64-bit |
| macOS | macOS 12 or later, Apple Silicon (M1 or later) |
| Linux | Debian or Ubuntu, x86-64 `.deb` package |

The installer is self-contained; Python is not required.

## Privacy and licensing

E.N.K.I.R.™ is commercial, closed-source software. It uses a signed, locally verifiable license key and Polar activation; the app can paste a key directly from your clipboard. The application checks `amara.zone` for updates. It does not collect telemetry; your assistants connect to their own providers as usual.

The installers may also be available as GitHub Releases. Wherever you download one, the installer still requires a valid Polar license to launch E.N.K.I.R.™.

## Links

- [Product page — free trial and purchase](https://amara.zone/en/products.html)
- [Setup guide and FAQ](https://amara.zone/en/faq.html)
