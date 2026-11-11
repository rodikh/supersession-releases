# Supersession

A Mac app for Claude Code, in alpha. Each session runs as it would in your terminal, under your own Claude login, and every turn becomes a card that says what Claude did, what needs you, and what to do next.

This repo holds only the builds. **[Download the latest build](https://github.com/rodikh/supersession-releases/releases/latest).**

## Install

Needs a Mac with Apple silicon on macOS 13 or later, and [Claude Code](https://docs.claude.com/en/docs/claude-code) installed and logged in. Sessions spend from your own Claude plan, the same as in a terminal.

1. From the [latest release](https://github.com/rodikh/supersession-releases/releases/latest), download `Supersession-<version>-arm64.zip` and, if you like, its `.sha256`; check it with `shasum -a 256 -c Supersession-<version>-arm64.zip.sha256` in the folder that has both.
2. Unzip it and move `Supersession.app` to Applications.
3. Open it. The build isn't signed, so macOS refuses the first time: on macOS 15 or later, open System Settings › Privacy & Security and click **Open Anyway**; on macOS 13 and 14, right-click the app and choose **Open**.

Your sessions are kept in `~/.supersession`, outside the app. To update, quit Supersession, replace the app with the new build, and open it; your sessions are kept. An older build won't open sessions a newer one has opened.

## What it never does

It never changes Claude Code's own settings, and plain `claude` in a terminal works exactly as before. It never uses an API key: everything goes through your Claude Code login.

## Known issues and feedback

What's still rough is in [KNOWN-ISSUES](KNOWN-ISSUES.md). To report a problem: Help › Report a Problem… in the app, read the zip it saves, and send the note and the zip to whoever sent you the link.
