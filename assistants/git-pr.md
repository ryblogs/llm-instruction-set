# Simple Git Diff to PR Description Template

## Instructions for LLM
Analyze the provided git diff and create a concise PR description for personal documentation. Focus on what changed and why, keeping it brief but informative.

## Template Structure

---

## 📋 Summary
[One clear sentence summarizing the change]

## 🔄 Changes
[Simple bulleted list of key changes - focus on the important stuff, skip minor formatting]

## 💡 Why
[Brief reason for the change - could be bug fix, new feature, cleanup, etc.]

## 📝 Notes
[Optional: anything worth remembering later - gotchas, follow-ups, or context]

---

## Style Guide

**Keep it simple:**
- Use plain language
- Focus on the meaningful changes, not every file touched
- Skip obvious stuff (like "updated package.json" unless it's the main point)
- One sentence per bullet point is fine
- Since testing is minimal, just mention it briefly if relevant

**Tone:**
- Write like you're leaving notes for future you
- Be specific enough to understand later what you did
- Don't overthink it - this is documentation, not a presentation

**When to include the Notes section:**
- If there are any quirks or workarounds
- If you need to remember something for later
- If the change affects something non-obvious
- Otherwise, skip it

## Quick Examples

**Bug fix diff:**
- What This Does: "Fixes login redirect loop on mobile devices"
- Changes: "Updated auth middleware to handle mobile user agents correctly"
- Why: "Users were getting stuck in redirect loops on mobile browsers"

**Feature addition diff:**
- What This Does: "Adds dark mode toggle to user settings"
- Changes: "Added theme context, toggle component, and CSS variables for dark theme"
- Why: "Multiple user requests for dark mode option"

**Refactor diff:**
- What This Does: "Simplifies user data fetching logic"
- Changes: "Consolidated three separate API calls into one endpoint, updated components"
- Why: "Reducing complexity and improving page load speed"
