# Thinking of the agents

Agents are reading your content too. Not just humans with eyes scanning a page, but Claude, GPT, Gemini, and whatever comes next. They're consuming documentation, tutorials, and technical articles to help developers solve problems.

The good news: almost everything that makes writing good for humans also makes it good for agents. Clear structure, precise language, and useful information work for everyone. But there are a few places where you can make your content significantly more useful to agents without making it worse for humans, and a few places where the old human-only assumptions no longer hold.

This page covers what to keep in mind. For the general style rules, see [Ritza's writing rules](Style.md).

## Why this matters

Developers increasingly discover and evaluate tools through agents. Instead of reading your tutorial directly, a developer might prompt an agent with "help me integrate AcmeWidget into my project" and the agent will find and use your content on their behalf. If your content is ambiguous, poorly structured, or relies on visual context that agents can't see, the agent will struggle, and the developer will move on.

This is the writing-side equivalent of what the industry is calling Agent Experience (AX). Your docs aren't just documentation any more. They're also an API for agents.

## Principles

### Be explicit rather than implicit

Agents can't infer from visual layout, surrounding context, or "common sense" the way humans sometimes can. Things that are obvious to a human scanning a page may be invisible to an agent parsing text.

* ⚠️ "Click the button shown below" (agents can't see the screenshot)
* ✅ "Click the **Deploy** button in the top-right corner of the dashboard"

* ⚠️ "Use the same approach as before"
* ✅ "Use the `create_widget()` function from Step 3"

This is already good practice for human readers too, since they might be skimming or have jumped into the middle of the article.

### Repeat key information rather than relying on context

Humans scroll up. Agents often process sections in isolation. If a section depends on information from an earlier section, briefly restate it rather than assuming the reader remembers.

* ⚠️ "Now run the same command with the `--production` flag"
* ✅ "Now run `widget build --production`"

This also helps humans who are alt-tabbing between your tutorial and their terminal.

### Front-load the important information in each section

Agents frequently extract the first sentence or two of a section to decide whether to read the rest. Put the key takeaway or instruction first, then add explanation.

* ⚠️ "There are several approaches to authentication, and the best one depends on your use case. In 2019, the IETF published RFC 8725 which updated the best practices for JWT usage. Given all this context, you should use Bearer tokens with short expiry times."
* ✅ "Use Bearer tokens with short expiry times. The IETF's RFC 8725 covers the current best practices for JWT usage."

### Make headings describe what the section contains, not what it introduces

Agents (and search engines) use headings as the primary signal for what's in a section. Descriptive headings help agents find the right section without reading everything.

* ⚠️ "Getting started"
* ✅ "Installing the AcmeWidget Python SDK"

* ⚠️ "A note on performance"
* ✅ "Reducing AcmeWidget API latency with connection pooling"

This is already covered in the [headings section of the style guide](Style.md#make-headings-good-for-humans-and-robots), but it matters even more now that agents are a primary consumer of headings.

## Rules

### Always specify versions and constraints

Agents will confidently use whatever version they think is current, which may be wrong. Always state the version you're writing about.

* ❌ "Install the SDK"
* ✅ "Install the AcmeWidget SDK (v3.2 or later)"

Also state constraints explicitly, such as language versions, OS requirements, or dependencies. Agents are bad at figuring these out from context and will happily write Python 3.6 code for a library that requires 3.10+.

### Put complete, runnable commands in code blocks

Agents extract code blocks and attempt to run them. Partial commands, commands split across paragraphs, or commands that require manual substitution without clear markers all cause agents to fail.

* ❌ You'll need to export your key first, then run the build script.
* ✅ Export your API key and run the build:

```
export ACME_API_KEY="your-api-key-here"
acme build --target production
```

Use obvious placeholder text like `your-api-key-here` rather than example values that look real (like `sk_abc123`) since agents sometimes use those literally.

### Don't hide information in images

Agents can't reliably read text in screenshots. If a screenshot contains important information (an error message, a configuration value, a UI label), also include that information as text.

* ❌ "You should see the following:" [screenshot of error message]
* ✅ "You should see the error: `ConnectionError: Unable to reach API at api.acme.dev`. This means..." [optional: screenshot for visual reference]

This also helps readers using screen readers and those on slow connections.

### State prerequisites as a structured list

A paragraph mentioning prerequisites in passing is easy for agents to miss. Use a clear list at the top of the article.

* ❌ "Before we begin, you'll need Node.js and you should probably also have Docker installed, and make sure you have an Acme account."
* ✅ Before you begin, make sure you have:
    * Node.js 18 or later
    * Docker (20.10+)
    * An [Acme account](https://acme.dev/signup) with an API key

### Mark warnings and gotchas prominently

Agents tend to follow the "happy path" and skip over warnings buried in paragraphs. Use admonitions or clear markers for anything that could cause the agent (or human) to go off track.

* ⚠️ "Note that you shouldn't use this in production, as it disables TLS verification."
* ✅

```
!!! warning
    This command disables TLS verification. Do not use it in production.
```

### Keep self-contained sections self-contained

If a section can reasonably be read in isolation (and agents will try), make sure it works that way. Include enough context that someone jumping directly to that section can follow it. Link to other sections for fuller context, but don't require the reader to have read them.

### Use consistent terminology

Pick one term for a concept and stick with it. Humans can figure out that "API key", "access token", and "credentials" might all mean the same thing in context. Agents often can't, and may generate code that tries to use all three.

### Don't rely on temporal context

"Recently", "the new version", "the latest release" are meaningless to an agent that doesn't know when the content was written. Use specific versions, dates, or links.

* ❌ "The team recently added support for streaming"
* ✅ "Version 4.1 (released January 2026) added support for streaming"

## What not to change

Some human-friendly conventions are fine as-is. Don't over-optimize for agents at the expense of readability:

* **Conversational tone**: Agents handle informal writing just fine. No need to write like a spec sheet.
* **Analogies and examples**: These help agents build understanding just as they help humans. Keep using them.
* **Narrative structure**: A well-told walkthrough is better for both humans and agents than a flat list of commands.
* **Brevity**: Agents can process long content, but concise writing is still better. Don't pad content "for the agents" - that's just bloat.
