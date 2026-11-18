# Gemini 4 Periodic Lab

A single-file chat web experiment that maps Gemini 4's Periodic Table models (`Hydrogen`, `Carbon`, `Neon`, `Argon`) to chemical stability and AI personas.

> **Note:** The author is under 18 and cannot generate a Gemini API key under the Terms of Service. If you have an API key and access to Gemini 4 endpoints, feel free to test it and share the results in the Issues.
>
> **Token Usage Warning:** Selecting both `Hydrogen (H)` and `Carbon (C)` runs a two-step relay (`gemini-4-hydrogen` for preliminary reasoning -> `gemini-4-carbon` for final synthesis), which consumes tokens across two API calls per message (including conversation history).

## Features

* **Hydrogen -> Carbon Relay**: When both `H` and `C` are selected, `gemini-4-hydrogen` first generates a brief preliminary note from a Hydrogen perspective, which `gemini-4-carbon` then integrates into the final answer from a Carbon perspective.
* **Interactive Chat & Mid-Conversation Reactions**: Add or remove atoms manually during a chat, or trigger spontaneous atomic mergers/dissociations as unstable molecules try to stabilize. State changes are logged in the chat and sent as context to the model.
* **Noble Gas Exclusivity (`Ne`, `Ar`)**: Selecting a noble gas deselects and disables all other elements. `Neon` acts as an energetic discharge tube; `Argon` acts lethargic per its Greek etymology (*argos*).
* **100+ Reference Molecules & Stability Personas**: Combining `H` and `C` evaluates stability against an internal database of over 100 hydrocarbons and carbon allotropes. Stable configurations adopt detailed chemical personas, while unstable configurations crave bonding or splitting mid-response.
* **Language Matching**: System prompts are generated in English while instructing the model to reply in the user's prompt language.

## Usage

1. Open `index.html` in any browser (or host via GitHub Pages).
2. Enter a Gemini API key to send live requests, or leave it blank to test the state transitions and demo responses.
