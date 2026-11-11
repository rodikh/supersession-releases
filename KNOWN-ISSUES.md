# Known issues

What's known to be rough in the current alpha build, so you don't have to report it. For anything not listed here, use Help › Report a Problem…, read the zip it saves, and send the note and the zip to whoever sent you the build.

## Before you install

- **Apple silicon only.** The build is for M-series Macs on macOS 13 or later; it won't run on an Intel Mac.
- **The build isn't signed.** macOS refuses it the first time; the [README](README.md#install) says how to open it anyway.
- **No automatic updates.** A new build comes as a new zip: quit Supersession, replace the app in Applications, and open it. Your sessions are kept.
- **Coming from Threadboard:** quit it before you open Supersession the first time, so your sessions move to `~/.supersession` at once; Threadboard.app can go once Supersession has opened them. An older Threadboard build won't see them after the move.
- **No going back a version.** Once a newer build has opened your sessions, an older one refuses to (it says so, and changes nothing). Keep the newer build.
- **Claude Code is required,** installed and logged in. Every session spends from your own Claude plan, the same as in a terminal.
- **Fish hasn't been tried on a real install;** zsh and bash have been. If you use fish and the setup screen says Claude Code is missing, give its path in Settings › Sessions.

## Cost

- **Each turn costs a little more than in a terminal:** Claude files a short report, and a digest of what's open goes with your next prompt. It's a few thousand tokens a turn, most of it cached; the exact figure hasn't been measured yet.
- **Coming back after an hour or more** costs more on the first turn, as it does in a terminal: the conversation's cache has expired and is written again.

## The card

- **A ✗ can be wrong.** When one command prints a pass and then a failure, the card reads it as failing. If a ✗ is wrong and no later run clears it, use `dismiss ✗` on it.
- **Changed files can be off** when Claude edits files with a shell command rather than its edit tools: the list is read from the command.
- **The summary can go stale.** The session's summary may lag a turn or two, and a session with no subject yet is titled by its first prompt.
- **`landed` can linger** on the card for many turns after a commit.
- **One choice can show as two decisions:** your click and Claude's note of it.
- **The context ring can read high** during a session's first turn, and settles when the turn ends.

## Asks and notifications

- **A permission request expires** when you quit or the app restarts mid-turn. A question stays and can be answered later.
- **No in-app toast** when a session you're not looking at finishes; its row's dot shows it.
- **No notification banners or Dock badge,** as the build isn't signed and macOS won't deliver them. When Claude waits on you while you're in another app, the Dock icon bounces once, and the sidebar's dot and the header show it.
- **A new question doesn't pull you off the Changes tab,** so it can sit unseen there; the sidebar's dot and the header show it.

## Elsewhere

- **⌘F finds only what's showing:** not folded history, folded cards or replies.
- **The sidebar's sessions can arrive a few seconds** after the window on launch.
- **An HTML artifact keeps its own white background** in dark mode.
- **A turn's line lists every approved shell command** separately, ungrouped.
