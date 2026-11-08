---
name: expert-designer
description: Explore a screen or interface idea through multiple distinct static HTML prototypes before product implementation. Use when the user wants visual alternatives to compare and refine, served locally with links between attempts and stored outside the target repository. Ordinary frontend implementation or a single prescribed screen does not require this workflow.
---

# Expert Designer

Turn an interface idea into navigable alternatives so the user can decide on a direction before implementation.

## Frame the exploration

Use the conversation, supplied references, and relevant existing product UI to understand the screen's purpose, content, audience, and constraints. Inspect the target repository read-only when it provides useful design context. Ask only about missing information that would materially change the alternatives.

Honor a requested number of alternatives. Otherwise, choose a small set of meaningfully different directions appropriate to the decision. Keep the content and functional goal comparable across options so the user can judge the design rather than unrelated feature differences.

Vary layout, hierarchy, density, typography, or interaction structure deliberately. A palette swap alone is not another design direction. Respect an established design system unless the request explicitly explores changing it.

## Keep prototypes outside the product repository

Create a dedicated folder in an allowed scratch workspace outside the target repository and its worktrees. Resolve its location before writing; do not use an ignored folder inside the target repository as a substitute. If no permitted external location is available, ask for one.

Build static HTML with CSS and optional presentation JavaScript. Prefer a lightweight solution using available tools; no application backend is needed. Use representative content and simulated interactions where they help evaluation. Never imply a simulated action is a working product integration.

Do not modify product source, dependency manifests, Git configuration, or ignore rules to support the exploration. Keep assets and server logs with the external prototypes. Use existing authorized assets or clearly fictitious content; do not copy secrets or private production data into mockups.

## Make every alternative reachable

Include a consistent navigation bar in every alternative with:

- A descriptive link to every attempt.
- An indication of the current attempt.
- An accessible label identifying the bar as prototype navigation.

Use relative links so the collection survives a change of port or directory. Keep the comparison navigation visually separate from the proposed product UI. An index page may summarize the directions, but it does not replace the links inside each attempt.

Support the intended viewport and basic responsive behavior. Use semantic controls, keyboard navigation, visible focus, and readable contrast so usability does not obscure the design comparison.

## Serve and verify

Serve only the dedicated prototype folder over HTTP using an available static server. Bind to loopback unless the user requests wider access. Choose an available port without stopping an unrelated process. Start the server in the background using the environment's supported process mechanism; on Windows, hide any helper window.

Verify that each alternative, its assets, and the navigation links load through the server. When browser tools are available, inspect the rendered options at the relevant viewport sizes and fix issues that prevent comparison. If visual inspection is unavailable, say what remains unverified.

Keep the server available for review as the environment permits. Report startup failures or session lifetime limits honestly; do not substitute an unverified URL or promise permanent availability.

## Hand over the decision

Provide the working local URL, the external prototype folder, and a short description of what distinguishes each direction. Include a practical way to stop or restart the server, using the actual process or command when available. Do not stop it immediately after delivering the links.

Refine or combine directions when the user gives feedback. Preserve earlier attempts unless replacing them is requested or clearly part of the agreed iteration. Selecting a prototype alone does not authorize changes to the product repository; implement it when the user requests implementation.
