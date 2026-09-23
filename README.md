<p align="center">
  <img src="icon.png" width="96" alt="Omny" />
</p>

<h1 align="center">Omny</h1>
<p align="center">Your own local-first AI assistant — chat, code, and files, with your data staying on your machine.</p>

---

## What is Omny?

Omny is a personal AI assistant that runs on your own computer. It talks to
the AI provider of your choice (Gemini, Claude, OpenAI, and others), but
everything else — your conversations, your documents, your project files —
stays in a database on your own machine. Nothing is uploaded anywhere except
the specific request you send to whichever AI provider you've configured.

You can use it two ways:
- **As an editor extension** (VSCodium / VS Code) — a chat panel that can
  also read, search, and (with your explicit approval on every change) edit
  files in your project.
- **In a browser** — the same assistant, as a local web app.

## What it can do

- **Chat with 10 different AI providers** — Claude, Gemini, OpenAI, Grok,
  DeepSeek, Mistral, Groq, Together, OpenRouter, and Ollama (fully offline,
  no account needed). Switch anytime from Settings.
- **Read and edit your project's files** (opt-in, per project) — Omny can
  look through your code, propose an edit or a new file, or propose running
  a command. Nothing is ever written to disk or executed until you click
  Approve.
- **Search your code** by exact text or, optionally, by meaning ("where do
  I handle a login?" finds the right function even without those exact
  words).
- **Attach images** to a chat message, and **upload documents** for Omny to
  reference while answering.
- **Works in English or Romanian** — switch anytime from Settings.

## Installing Omny (Windows)

1. Go to the **Releases** page of this repository (see the sidebar) and
   download the latest **`OmnySetup.exe`**.
2. Run it. No administrator rights are needed — it installs into your own
   user folder, and adds a shortcut to your Start Menu.
3. On the installer's last page, leave "Launch Omny" and "Open in browser"
   checked and click Finish. A browser tab opens automatically to Omny's
   first-time setup screen.

### First-time setup

The setup screen walks you through two short steps:

1. **Database** — click **Quick start** and Omny prepares a small, private
   database for itself automatically. (If you're technical and already run
   your own PostgreSQL, there's an "I already have a database" option too.)
2. **AI provider key** — add one API key so Omny has an AI to talk to.
   - The easiest, free option: **Gemini**. Click the link on screen to
     generate a free key at [aistudio.google.com/apikey](https://aistudio.google.com/apikey),
     paste it in, done.
   - Prefer Claude, OpenAI, or another provider instead? Open "I have a
     different provider" on the same screen and pick one — each has a
     direct link to where you get a key.
   - You can also skip this step and add a key later from **Settings**.

That's it — Omny is ready to chat.

### Installing the editor extension (optional)

If you write code and want Omny as a chat panel inside VSCodium or VS Code:

- **From the Marketplace** (once published): search **"Omny"** in the
  Extensions panel of Open VSX-based editors (VSCodium, Cursor, etc.) and
  install it directly.
- **Manually**: download the `.vsix` file from this repository's Releases
  page, then either:
  - drag it onto the Extensions panel, or
  - run `codium --install-extension omny-vscodium-<version>.vsix`
    (or `code --install-extension ...` on VS Code itself).

The extension talks to the same Omny backend — if it's already running (you
just installed it above), the extension finds it automatically the moment
you open the Omny icon in the activity bar.

## Quick start

- **Open the chat** — the web tab that opened during setup, or the Omny
  icon in your editor's activity bar.
- **Pick a model** from the picker next to the send button (or leave it on
  "Auto" — it picks a fast/free model for short messages and a stronger one
  for longer ones).
- **Turn on Agentic mode** (toggle in the composer) once you've pointed a
  project at a folder on disk, if you want Omny to read/search/edit files
  for you — every file change still needs your explicit click to apply.
- **Attach an image** with the "+" button or by pasting (Ctrl+V) directly
  into the message box.
- **Explorer panel** — browse, search (by name, content, or meaning), and
  open files in the current project without leaving the chat.
- **Settings** — add/remove provider keys, pick a custom model name per
  provider, switch language, back up or restore all your data as one JSON
  file.

## Uninstalling

Use **Add or Remove Programs** in Windows Settings, or run "Uninstall Omny"
from the Start Menu group created at install time. This removes the
application files; your database and uploaded files are left in place
unless you remove them separately — see Settings → Backup and recovery for
exporting everything first if you want a copy.

## Getting help

Something not working? Open an **Issue** on this repository with what you
were doing and what happened — screenshots help.

## Privacy

Omny doesn't collect telemetry or send your data anywhere except the AI
provider you've explicitly configured, for the specific message you send.
Your conversations, documents, and project data live in a local database on
your own machine.
