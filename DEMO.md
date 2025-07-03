# Simple Agent Memory

## LLMs Have Amnesia

...but you can hack around it.

## Intro

Cline Memory Bank Methodology:

> The Memory Bank methodology is an open approach to AI context management
> that can be adapted to different tools and workflows.

...created by the Cline team, but it works in VSCode with GitHub Copilot - or any other AI-enabled editor. Nice!

- <https://docs.cline.bot/prompting/cline-memory-bank>

- <https://cline.bot/blog/memory-bank-how-to-make-cline-an-ai-agent-that-never-forgets>

## What you need

- A memory spec: this is just a markdown file. Mine is at `~/.ai/memory.spec.md`. Copy and paste from the Cline documentation. Make changes to it if you like. It provides instructions for a tool-enabled LLM to create a text-file-based memory.

- `.github/copilot-instructions.md`: This file is supported by the GitHub Copilot extension. It is used to provide workspace-specific custom instructions to Copilot. **But I haven't figured out yet how to make it work automatically without nudging the LLM to follow it. You'll see what I mean.**

- `.vscode/settings.json`: This is the VSCode settings file for the workspace. You can define MCP servers here. We'll use it to set up the `mcp/filesystem` server using Docker. **For some reason, the MCP config in this file only works if you open the project through File --> Open Folder. It doesn't work if it's a workspace.** `¯\_(ツ)_/¯`

## Voilà

Now you have a simple memory system for your local AI agent.
