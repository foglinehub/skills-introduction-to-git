# Claude Code Folder Setup — Handoff Guide

**Purpose:** Help a new user (referred to below as "Mom") set up and organize her
Claude Code folders the same way the sender already has them organized.

**Two audiences read this document:**
1. **The Claude assistant** helping with setup — read the section
   *"For the Claude Assistant"* first. It tells you what to build and how to
   behave.
2. **Mom** — the numbered *"Walkthrough"* steps are written in plain language so
   she can follow along, or so the assistant can read them to her one at a time.

---

## The Big Picture (what we're building and why)

Claude Code works best when it has a tidy "home base" folder on the computer.
Inside that home base we keep a few special files and folders. Each one has a
job:

| Piece | What it is | Why it matters |
|---|---|---|
| **`CLAUDE.md`** | A plain-text "instructions & memory" file | Claude reads this **automatically** every time it starts. It's how Claude "remembers" who Mom is and how she likes things done. |
| **`my-voice/`** | A folder holding examples and notes about how Mom writes and talks | So anything Claude writes *for* Mom sounds like Mom — not like a robot. |
| **`INDEX.md`** | A table-of-contents file | A map of the whole setup so Mom (and Claude) can find anything fast. |
| **`projects/`** | One sub-folder per thing Mom is working on | Keeps each project's files separate and organized. |
| **`reference/`** | A folder for reusable info (accounts, preferences, templates) | A single place to store things Claude should look up. |

Think of it like a well-organized kitchen: `CLAUDE.md` is the recipe card taped
to the fridge, `my-voice/` is Mom's personal cookbook, `INDEX.md` is the label on
every drawer, and `projects/` are the meals currently being cooked.

---

## The Folder Structure (the target)

Here is exactly what we're going to create. Everything lives inside one main
folder. On a Mac this can live in the user's Documents; on Windows the same.

```
ClaudeHome/                      ← the main "home base" folder
│
├── CLAUDE.md                    ← master instructions + memory (auto-read)
├── INDEX.md                     ← the map / table of contents
│
├── my-voice/                    ← how Mom writes and sounds
│   ├── voice-guide.md           ← the rules: tone, phrases she uses/avoids
│   └── samples/                 ← real examples of her writing
│       ├── email-example-1.md
│       └── note-example-1.md
│
├── projects/                    ← one folder per project
│   ├── _TEMPLATE/               ← copy this to start a new project
│   │   └── CLAUDE.md
│   └── example-project/
│       ├── CLAUDE.md            ← notes specific to THIS project
│       └── (project files...)
│
└── reference/                   ← reusable info Claude can look up
    ├── preferences.md           ← how Mom likes things done
    └── contacts.md              ← people/info she refers to often (optional)
```

> **Note on the name:** `ClaudeHome` is just a suggestion. Any name works
> (`Claude`, `MyClaude`, etc.). Pick one and keep it consistent everywhere.

---

## What each piece contains (the important details)

### 1. `CLAUDE.md` — the master file (MOST IMPORTANT)
This is the single most important file. Claude Code automatically loads it as
memory whenever it starts working in this folder. **Keep it short and clear** —
it's read every time, so bullet points beat paragraphs.

A good starter `CLAUDE.md` looks like this:

```markdown
# About Me
- My name is [Mom's name].
- I use Claude for [email, writing, organizing photos, etc.].
- I'm not a programmer — explain things simply and avoid jargon.

# How I Like Claude to Work
- Always explain what you're about to do before doing it.
- Ask before deleting or changing any file.
- When you write anything for me, match my voice — see the `my-voice/` folder.

# My Setup
- This is my home base folder.
- See INDEX.md for a map of everything.
- Reusable info (preferences, contacts) is in the `reference/` folder.
```

**Key detail:** There can be *more than one* `CLAUDE.md`. The one at the top
(home base) holds general info. Each project folder can have its *own*
`CLAUDE.md` with notes just for that project. Claude reads the closest one it can
find, so project-specific notes automatically apply when working in that project.

### 2. `my-voice/` — sounding like Mom
- **`voice-guide.md`** — plain-language rules about how Mom writes:
  - Tone (warm? formal? funny?)
  - Words and phrases she likes to use
  - Words and phrases she never uses
  - Sign-offs she uses in emails ("Love, Mom", "Best,", etc.)
- **`samples/`** — 2–5 real examples of things Mom actually wrote (an email, a
  note, a message). Examples teach Claude her voice better than rules alone.

**Key detail:** In `CLAUDE.md`, tell Claude to check `my-voice/` before writing
anything on Mom's behalf. That one instruction is what makes the whole thing
work.

### 3. `INDEX.md` — the map
A simple list of what's where, so nothing gets lost. Example:

```markdown
# Index — My Claude Home Base

- CLAUDE.md ......... My main instructions and memory.
- my-voice/ ......... How I write; check before drafting anything for me.
- projects/ ......... Everything I'm currently working on.
- reference/ ........ Preferences, contacts, and reusable info.

## Current Projects
- example-project — [one line describing it]
```

**Key detail:** Update `INDEX.md` whenever a new project is added. It's the
30-second answer to "where is everything?"

### 4. `projects/` — the work
- One folder per project. Keep names short and clear
  (`holiday-letter`, `photo-organizing`, `book-club`).
- Copy the `_TEMPLATE/` folder to start a new project — that way every project
  begins with its own `CLAUDE.md`.
- A project's `CLAUDE.md` holds only what's special about *that* project (goal,
  key files, any special instructions).

### 5. `reference/` — reusable info
Things Claude should look up rather than guess:
- **`preferences.md`** — how Mom likes documents formatted, times she's
  available, tools she uses.
- Anything else she refers to repeatedly.

Keep anything sensitive (passwords, financial details) **out** of these files.

---

## For the Claude Assistant

*(This section is written for the Claude account that will help Mom. Read it
before starting.)*

**Your job:** Walk Mom through creating the folder structure above, one step at a
time, and fill each file with content that's actually about her. She is not a
programmer — be patient, explain every step in plain words, and never assume
technical knowledge.

**How to behave:**
- Do **one step at a time**. Wait for her to confirm before moving on.
- Before creating or changing anything, say what you're about to do in one
  sentence.
- **Never delete or overwrite** an existing file without asking first.
- When you reach the `CLAUDE.md`, `my-voice/`, and `preferences.md` files,
  **interview her** — ask the questions, then write the answers into the files
  for her. Don't hand her a blank file to fill in.
- If she already has some of these folders, adapt to what exists instead of
  starting over. Look before you write.
- Confirm at the end by reading back the final structure and offering to make a
  first test project.

**What "done" looks like:** The folder structure above exists, `CLAUDE.md` and
`INDEX.md` are filled in with real information about Mom, `my-voice/` has at least
the voice-guide plus one sample, and she has run Claude Code once in the folder to
confirm it reads `CLAUDE.md`.

---

## Walkthrough (the steps for Mom)

*The assistant should do these together with Mom, one at a time.*

**Step 1 — Make the home base folder.**
Create one folder to hold everything. Suggested name: `ClaudeHome`. Put it
somewhere easy to find, like Documents.

**Step 2 — Create the master `CLAUDE.md` file.**
Inside `ClaudeHome`, create a file named exactly `CLAUDE.md` (capital letters,
`.md` at the end). The assistant will ask Mom a few questions (her name, what she
uses Claude for, how she likes things explained) and write the answers in.

**Step 3 — Build the `my-voice/` folder.**
Create a folder called `my-voice`. Inside it:
- Create `voice-guide.md`. The assistant asks how Mom likes to sound and writes
  it down.
- Create a `samples` folder and drop in 2–3 real examples of Mom's own writing
  (an email or note she's happy with).

**Step 4 — Create `INDEX.md`.**
Back in `ClaudeHome`, create `INDEX.md` and list what each folder is for. This is
the map.

**Step 5 — Set up `projects/`.**
Create a `projects` folder. Inside it, create a `_TEMPLATE` folder with an empty
`CLAUDE.md` inside. To start any new project later, Mom just copies `_TEMPLATE`
and renames it.

**Step 6 — Create `reference/`.**
Create a `reference` folder with a `preferences.md` file. The assistant asks how
Mom likes things done (formatting, timing, tools) and writes it in.

**Step 7 — Test it.**
Open Claude Code in the `ClaudeHome` folder and ask it: *"What do you know about
me?"* If it answers using the `CLAUDE.md` details, everything is wired up
correctly. 🎉

**Step 8 — First real project (optional but recommended).**
Copy `_TEMPLATE` into `projects/`, rename it to something real (e.g.
`holiday-letter`), and let Claude help with an actual task — using Mom's voice
from `my-voice/`.

---

## Quick Rules to Remember

1. **`CLAUDE.md` is read automatically** — keep it short and current.
2. **Every project can have its own `CLAUDE.md`** — specific notes live with the
   project.
3. **`my-voice/` makes Claude sound like Mom** — tell `CLAUDE.md` to check it
   before writing.
4. **`INDEX.md` is the map** — update it when things change.
5. **Never store passwords or sensitive details** in these files.
6. **When in doubt, ask** — the assistant should confirm before changing
   anything.

---

*Hand this whole document to the helping Claude account and say: "Please set this
up with my mom, following the instructions inside." That's all it needs.*
