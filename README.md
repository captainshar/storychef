# StoryChef

An AI-assisted writing system that uses Claude as an **interviewer and editor** — not a ghostwriter.

## The Idea

Most AI writing tools generate content for you. StoryChef does the opposite. It treats your story like a meal: **you grew the ingredients** (your memories, ideas, imagination), and the tool helps you figure out what you've got, what goes together, and how to serve it.

Claude asks questions. You answer. The story emerges from what's already inside you.

## How It Works

StoryChef has four modes that move your project from raw material to finished work:

| Mode | What Happens | Chef Metaphor |
|------|-------------|---------------|
| **Interview** | Claude asks questions, you answer, material accumulates | Sourcing ingredients — what's in the pantry? |
| **Craft** | Shape raw material into structure, arcs, and chapters | Mise en place — what goes with what, in what order? |
| **Draft** | You write; Claude offers structural observations | Cooking — you're at the stove, chef advises on technique |
| **Edit** | Claude gives craft feedback on your drafts | Tasting and plating — balance, seasoning, presentation |

The critical rule: **Claude never generates your story content.** No dialogue, no scenes, no plot points. It asks questions, tracks what's established, identifies gaps, and offers categorical suggestions when you're stuck.

## Getting Started

### 1. Copy this project

Clone or download this repository. Each book gets its own copy.

### 2. Choose your genre module

Copy the relevant file from `/genres/` and read through it. The genre modules add interview layers and craft frameworks specific to your type of project:

- **`genres/memoir.md`** — Personal narrative, life stories, autobiographical writing
- **`genres/fiction.md`** — Novels, short stories (literary or genre)
- **`genres/creative-nonfiction.md`** — Personal essays, narrative journalism, hybrid forms

Don't see your exact genre? These are starting points. See [Deep Research](#deep-research) below.

### 3. Fill out your book bible

Open `book-bible.md` and fill in what you know. Start with the basics: title, type, core question, main character(s). Leave the rest blank — you'll fill it in through interviews.

### 4. Start a conversation

Open the project in Claude Code (or any Claude-based tool that reads CLAUDE.md). Claude will read the project files and start interviewing you.

If Claude starts generating story content, say **"interviewer mode"** to reset.

## Deep Research

The genre modules provide general starting points, but the best results come from researching your *specific* type of project. A tragicomic divorce memoir has different beats than a coming-of-age immigrant story. A psychological thriller needs different craft frameworks than a cozy mystery.

**`templates/genre-research-prompt.md`** contains a customizable prompt template you can use with any deep-research AI tool (Gemini Deep Research, Perplexity, etc.) to generate a comprehensive editorial guide for your exact genre niche.

The workflow:
1. Customize the research prompt for your specific project
2. Run it through a deep-research tool
3. Distill the results into your project's `notes/editorial-guide.md`
4. Claude will reference this guide during Craft and Edit modes

This is how the original project that inspired StoryChef was built — with deep research on "tragicomic divorce memoir" that surfaced specific beats, tonal techniques, and reference works that generic writing advice never would have found.

## Key Files

| File | Purpose | When to Update |
|------|---------|----------------|
| `CLAUDE.md` | Instructions for Claude | Rarely (add genre-specific rules as needed) |
| `book-bible.md` | Source of truth for your story | When major elements are decided |
| `session-state.md` | Where you are right now | Every session |
| `notes/editorial-guide.md` | Craft frameworks for your project | As you research and discover what works |
| `/templates/` | Reference templates | Never (reference only) |
| `/chapters/` | Your drafted chapters | As you write |
| `/notes/` | Research, fragments, transcripts | Ongoing |

## Tips

- **Update the bible when things are DECIDED**, not just discussed. There's a difference between exploring an idea and committing to it.
- **Capture exact wording.** When you say something well in an interview, that phrasing is gold. Claude should preserve it verbatim in `notes/raw-transcripts.md`.
- **Don't rush to Draft mode.** The Interview → Craft pipeline is where most of the real work happens. Drafting with thin ingredients produces thin writing.
- **The session state is your save point.** Keep it current so you can pick up where you left off, even weeks later.
- **Genre research pays off.** Spending time up front with the research prompt template gives Claude much better guidance during Craft and Edit modes.

## Project Structure

```
storychef/
├── CLAUDE.md               # Instructions for Claude
├── README.md               # This file
├── book-bible.md           # Source of truth for your story
├── session-state.md        # Current progress checkpoint
├── genres/                 # Genre-specific modules
│   ├── memoir.md
│   ├── fiction.md
│   └── creative-nonfiction.md
├── templates/              # Reference templates (don't edit)
│   ├── interview-quick-reference.md
│   ├── book-bible-template.md
│   ├── session-state-template.md
│   ├── editorial-guide-template.md
│   └── genre-research-prompt.md
├── chapters/               # Your drafted chapters
└── notes/                  # Research, transcripts, fragments
```

## Origin

StoryChef was developed through real use on a memoir project. The original system started as a 3-mode interview template. After months of actual writing sessions, it evolved: Craft mode emerged to bridge the gap between raw interviews and drafting, real-time capture replaced end-of-session updates, voice-locking techniques were added, and editorial frameworks became living documents rather than static references.

Everything in this system was learned by doing the work.

## License

MIT
