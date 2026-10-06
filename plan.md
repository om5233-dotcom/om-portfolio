# Om Wanjari Portfolio — Implementation Plan

## Product scope

Create a responsive, single-page portfolio for Om Wanjari using the supplied resume as the source of truth. The site includes a resume-derived introduction, education, experience, project showcase, technical skills, contact links, and a downloadable local copy of `Om_Wanjari_Resume.pdf`. It is a static Vite app prepared for Vercel with the supplied `vercel.json`. There is no `index.ts`, Vite endpoint, API key, backend, or LeetCode link.

## Design direction

- **Design movement:** Editorial Blueprint — a print-inspired developer portfolio with the discipline of a technical brief.
- **Core principles:** clear hierarchy, warm human texture, confident restraint, and purposeful utility.
- **Color philosophy:** blueprint blue anchors trust and technical clarity; warm paper keeps the page approachable; orange and ink accents create moments of energy without competing with the content.
- **Layout paradigm:** asymmetrical editorial spreads with a narrow utility rail, large left-aligned statements, and outlined case-study panels rather than a centered card grid.
- **Signature elements:** blueprint-style section numbering, hairline rules, and a compact “brief” panel that makes the resume feel like a designed document.
- **Interaction philosophy:** navigation is direct and quiet; links use small arrow cues and underline transitions; hover states reinforce the editorial rule system.
- **Animation:** small fade/slide-in reveals on content blocks, a gentle floating mark in the hero brief, and no motion that competes with reading or accessibility.
- **Typography system:** Space Grotesk for display and interface copy, with a system sans fallback; compact uppercase labels use tracking and small sizes to feel like document annotations.
- **Brand essence:** a student builder turning AI and chatbot ideas into useful, understandable software. Personality: thoughtful, curious, practical.
- **Brand voice:** direct, optimistic, and specific. Example lines: “I build useful ideas into clear, working software.” and “Let’s make the next idea easier to use.”
- **Wordmark & logo:** a compact `OW` monogram inside a blueprint-blue outlined square, used as a document stamp rather than a generic text logo.
- **Signature brand color:** blueprint blue `#164E63`.

## Implementation approach

- **Frontend:** React with Vite, plain JavaScript and CSS; no server-side code or API routes.
- **Content:** hard-coded resume-derived content in `src/main.jsx` for a fast, portable static build.
- **Assets:** the supplied PDF is copied to `public/assets/Om_Wanjari_Resume.pdf`. No unavailable images are invented or requested.
- **Deployment:** `vercel.json` preserves the requested Vite build, dev, install, framework, output, and production environment settings. The Vite build writes to `dist/public`.
- **Discoverability:** `public/manus-routes.json` declares the `/` page for the managed preview workflow; `index.html` includes page metadata and social-friendly basics.

## Project structure

- `index.html` — Vite entry document, metadata, and font loading.
- `vite.config.js` — Vite build output configuration for `dist/public`.
- `src/main.jsx` — portfolio sections, resume content, navigation, and link actions.
- `src/styles.css` — responsive Editorial Blueprint visual system, layout, motion, and accessibility states.
- `public/assets/Om_Wanjari_Resume.pdf` — local downloadable resume.
- `public/manus-routes.json` — managed route manifest.
- `public/logo.svg` — local OW stamp mark and favicon source.
- `app.config.ts` — project logo metadata for Manus project presentation.
- `vercel.json` — user-supplied Vercel configuration.
