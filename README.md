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

Two critical rules:

1. **Claude never generates your story content.** No dialogue, no scenes, no plot points. It asks questions, tracks what's established, identifies gaps, and offers categorical suggestions when you're stuck.

2. **Capture first, respond second.** Before each conversational response, Claude captures your raw material into project files and commits. Your exact words — in the moment you say them — are the most valuable thing in this process. They can't be reconstructed later with the same voice and specificity.

## Getting Started

### Option A: Claude Desktop (Recommended)

The simplest way to use StoryChef. No command line needed.

1. **Install Claude Desktop** from [claude.ai/download](https://claude.ai/download) (requires a Claude Pro, Max, or Team subscription)
2. **Download this project** — click the green "Code" button on GitHub, then "Download ZIP." Unzip it.
3. **Move the folder** to somewhere that syncs to the cloud — your Documents folder works (iCloud syncs it automatically on Mac). Google Drive or Dropbox folders work too. This way your project is backed up and accessible from anywhere.
4. **Rename the folder** to your book's name (or "untitled-book" if you don't have one yet)
5. **Open Claude Desktop**, switch to **Code** mode, and open your project folder
6. **Say hello.** Claude will introduce itself and walk you through getting started. You don't need to fill anything out first — the onboarding conversation handles it.

If Claude starts generating story content instead of asking questions, say **"interviewer mode"** to reset.

### Option B: Claude Code (Command Line)

If you're comfortable with a terminal:

```
git clone https://github.com/captainshar/storychef.git my-book-title
cd my-book-title
claude
```

Say hello and go.

### Option C: Claude.ai (Web, No Install)

See `claude-ai/setup-guide.md` for instructions on using StoryChef as a Claude.ai Project. This works in your browser with no install, but requires manual saving between sessions.

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
