# StoryChef for Claude.ai — Setup Guide

A version of StoryChef that works inside Claude.ai Projects. No command line, no code, no technical setup — just a conversation that gradually turns into a book.

## What You Need

- A Claude account (Pro, Max, Team, or Enterprise — Projects require a paid plan)
- About 10 minutes to set up

## Setup

### 1. Create a New Project

1. Go to [claude.ai](https://claude.ai)
2. Click **Projects** in the sidebar
3. Click **Create Project**
4. Name it after your book (or "Untitled Book" if you don't have a title yet)
5. Add a description if you want (optional)

### 2. Set the Custom Instructions

1. In your project settings, find **Custom Instructions** (sometimes called "Project Instructions")
2. Open the file `system-prompt.md` from this folder
3. Copy the entire contents and paste it into the custom instructions field
4. Save

### 3. Upload the Reference Files

Upload these files to your project's **Knowledge** section:

**Required:**
- `interview-quick-reference.md` (from `templates/`)

**Upload the genre module(s) that fit your project:**
- `memoir.md` (from `genres/`) — for personal narrative, life stories
- `fiction.md` (from `genres/`) — for novels and short stories
- `creative-nonfiction.md` (from `genres/`) — for essays, narrative journalism

You can upload all three if you're not sure yet.

**Optional but recommended:**
- `editorial-guide-template.md` (from `templates/`) — useful when you're ready to build craft frameworks
- `genre-research-prompt.md` (from `templates/`) — if you want to do deep genre research
- `book-bible-template.md` (from `templates/`) — the full template with all fields (Claude has the basics in its instructions, but this gives it the extended version)

### 4. Start Talking

Click **New Chat** in your project and say hello. StoryChef will introduce itself and start asking about your book.

## How Sessions Work

Each conversation in Claude.ai is independent — Claude doesn't automatically remember previous chats within the project. StoryChef handles this with artifacts:

### During a Session
- StoryChef maintains a **Book Bible** artifact (your story's source of truth) and **Session Notes** (raw captured material)
- These update as you talk — you'll see them appear in the artifacts panel

### Ending a Session
When you're done for the day, tell StoryChef you're wrapping up. It will:
1. Update your Book Bible with everything decided
2. Create a **Session Handoff** with where you left off and what to explore next

### Starting the Next Session
At the beginning of your next chat, do ONE of these:
- **Easiest:** Copy the Book Bible and Session Handoff text from the previous chat's artifacts and paste them into your first message: "Here's where we left off: [paste]"
- **Cleanest:** Download the artifacts, re-upload them to the project's Knowledge section (replacing older versions), then just say "hello" — Claude will read them from the knowledge files
- **Quickest:** Just describe where you left off in your own words — "Last time we were working on the origin chapter and figured out the timeline"

Any of these work. The first two are more precise; the third is fine if you're comfortable with Claude rebuilding context from your description.

## Tips

- **Talk naturally.** You don't need to structure your thoughts. Stream of consciousness is fine — StoryChef captures and organizes it.
- **Your exact words matter.** StoryChef preserves your phrasing because your voice IS the book. If you say something well, it gets flagged as a "key line."
- **Say "interviewer mode" if Claude starts writing FOR you.** It should be asking questions, not generating your content.
- **You don't have to finish a thought.** If you trail off or change direction, that's fine. StoryChef will follow where the energy goes.
- **Genre research is worth doing.** When StoryChef offers you the option to run a deep research prompt, consider taking it. The results dramatically improve the craft guidance it can give you later.
- **Save your Book Bible.** This is the most important artifact. Everything else can be reconstructed, but the bible is your accumulated source of truth. Save it somewhere (a doc, a note, wherever) after significant sessions.

## What's Different from the CLI Version

If you've seen the Claude Code version of StoryChef, here's what changes:

| Feature | Claude Code (CLI) | Claude.ai (Projects) |
|---------|------------------|---------------------|
| File management | Automatic — updates files directly | Manual — you save artifacts between sessions |
| Git history | Automatic commits | Not available |
| Session continuity | Automatic via session-state.md | Manual — paste or upload previous artifacts |
| Raw transcript capture | Written to files in real-time | Maintained as artifact during session |
| Interface | Terminal with tool-use output | Clean chat interface |
| Technical skill needed | Comfortable with command line | Can use a web browser |

The core methodology is identical. The interview approach, modes, genre modules, and craft frameworks are the same. The difference is just how state is managed between sessions.

## Troubleshooting

**Claude is writing my story for me instead of asking questions.**
Say "interviewer mode" to reset. If it keeps happening, remind it: "You're StoryChef — ask questions, don't generate."

**I lost my Book Bible between sessions.**
Describe what you remember about your project. StoryChef can help you reconstruct it through conversation, but it won't be as precise. This is why saving the artifact matters.

**Claude doesn't seem to know about my genre.**
Make sure you uploaded the relevant genre module to the project's Knowledge section. If your specific subgenre isn't covered, use the genre research prompt template to do deep research and bring the results back.

**The artifacts aren't updating.**
Ask Claude directly: "Update the Book Bible with what we just established." Sometimes you need to prompt artifact updates explicitly.
