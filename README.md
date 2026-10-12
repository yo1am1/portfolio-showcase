# Yehor Trepalin's portfolio

I'm Yehor Trepalin. I'm building my résumé as a website where you can read about my work and ask questions. The project brings together my work on a browser interface, a Python backend and agents that use tools to answer questions.

[Visit the website](https://yehor-trepalin.up.railway.app/) · [LinkedIn](https://www.linkedin.com/in/yehor-trepalin/) · [GitHub](https://github.com/yo1am1)

The public website currently opens the Tea shop demo. The portfolio edition, including the résumé workspace and the paper interface described below, is still in development.

## Tea Shop Assistant

The Tea shop is the first demo to explore. It gives the assistant a concrete task: help someone choose a product from a catalog and decide what to put in a demo cart.

Ask Tea for a recommendation, compare products, or check a brewing method. Give it a budget or a caffeine preference to narrow the search. Cart changes wait for your approval.

A few questions to start with:

- "Find a caffeine-free tea with citrus notes."
- "Compare two green teas under 10 EUR."
- "How should I brew an oolong?"

The catalog, prices and shop policies are synthetic. There are no real orders, payments or deliveries.

## What went into it

The frontend uses Svelte and TypeScript. A Python backend built with FastAPI and LangGraph handles conversations and tool calls. Building the project has meant connecting the interface to those workflows, deciding which actions need approval, and checking how the application handles failures.

Some decisions behind the demo:

- Catalog and policy lookups give Tea records to work from. Replies pass through checks before they reach the chat.
- Cart changes require a separate approval, so the visitor can review an action before it happens.
- A read-only Model Context Protocol (MCP) interface makes catalog lookups available to compatible assistants without giving them control over carts or conversations.

Verification includes automated tests with synthetic inputs and browser checks of the interface. The application source stays private; this repository explains the work and lets you explore the result through the website.

## The portfolio edition

| Space | What it's for |
| --- | --- |
| Portfolio | My résumé beside a conversation about my background and skills. |
| Main | A coordinator that brings in Portfolio or Tea when a question needs a specialist. |
| Tea | The shop demo, with product search, comparisons, brewing advice and a demo cart. |

The résumé is awaiting publication in this edition. Current Portfolio sample answers are labelled synthetic and do not describe my career. Projects is planned for a later version.

I wanted the interface to feel like paper and fabric. Folded corners turn the pages, handwritten notes point to useful places, and small movements give the lettering a stop-motion feel. Coraline (2009) is a visual reference for this design.

<details>
<summary>How the agents work together</summary>

In the portfolio edition, agents exchange requests through a private Agent-to-Agent (A2A) transport. Their replies show which agent wrote them. Work has limits so delegation cannot continue indefinitely.

</details>

## Contact

You can reach me through [LinkedIn](https://www.linkedin.com/in/yehor-trepalin/) or email [bigdiebam@gmail.com](mailto:bigdiebam@gmail.com). My other public projects are on [GitHub](https://github.com/yo1am1).

