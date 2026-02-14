# Using the Anti-Smells Folder

This folder contains **pasteable** text snippets to keep AI chats
disciplined (scope-locked, approval-gated).

## Files

### 1) `chat-start-context.md`

**What it is:** The main behavioral contract (the rules).\
**When to use:** At the very start of a new chat.

**How to use:** 1. Copy the contents of `chat-start-prompt.md`.
2. Upload `chat-start-context.md`. to the chat
3. Press enter


------------------------------------------------------------------------

### 2) `chat-start-prompt.md`

**What it is:** A short "load the contract" instruction.\
**When to use:** First message of a new chat, right before uploading the
context file.

------------------------------------------------------------------------

### 3) `chat-getting-loose-prompt.md`

**What it is:** A mid-chat reset when the assistant starts bundling
decisions, drifting, or moving too fast.\
**When to use:** The moment the chat starts feeling "loose," but before
it's fully off the rails.

**How to use:** 1. Paste `chat-getting-loose-prompt.md`. 2. (Optional
but recommended) Re-upload `chat-start-context.md` with the message.

------------------------------------------------------------------------

### 4) `chat-clearly-drifting-prompt.md`

**What it is:** A hard stop escalation when the assistant is clearly
violating scope/approval rules.\
**When to use:** After a clear drift (unrequested changes, assumptions,
multi-question pileups, or unscoped rewrites).

**How to use:** 1. Paste `chat-clearly-drifting-prompt.md`. 2. Re-upload
`chat-start-context.md`. 3. Require exactly **one** clarifying question
next.

------------------------------------------------------------------------

## Recommended Workflow

-   **New chat:** `chat-start-prompt.md` → `chat-start-context.md`
-   **Mid-chat drift (early):** `chat-getting-loose-prompt.md` →
    (optional) `chat-start-context.md`
-   **Mid-chat drift (severe):** `chat-clearly-drifting-prompt.md` →
    `chat-start-context.md`

## Tip: Keep It Fast

If you want the smallest copy/paste, you can paste: -
`chat-start-prompt.md` - then the contract (`chat-start-context.md`)

...and only use the reset prompts when needed.
