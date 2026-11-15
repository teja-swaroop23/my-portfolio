# Project memory

## Product intent & audience

- Personal portfolio website for a Hyundai Mobis GET (Graduate Engineer Trainee) in the LKA/PDW department, ADAS Application Software Group
- Goal: showcase ADAS expertise, automotive engineering work, and GitHub projects
- Audience: recruiters, engineering peers, potential employers

## Brand personality & voice

- Automotive engineering professional with technical credibility
- Visually impressive ("flex") but grounded in real ADAS domain work
- Confident, modern, tech-forward tone

## Visual design & UX direction

- **3D scene**: Three.js car model with glowing headlights/taillights/underglow, spinning wheels, ADAS sensor beams (front camera cone for LKA, rear ultrasonic beams for PDW), animated lane lines, floating particles, mouse parallax
- **Background**: dark blue grid, automotive aesthetic
- **Color scheme**: blue/cyan automotive (replaced earlier green PCB theme)
- **ADAS diagrams**: animated LKA visualization (lane detection + steering correction) and PDW visualization (ultrasonic sensor waves, obstacle detection, proximity zones)
- **Sections**: hero (Hyundai Mobis GET + LKA/PDW), experience timeline (Mobis GET, KL University degree 9.5 CGPA, diploma), live GitHub repo cards with language indicators, scroll-reveal animations
- **Responsive**: mobile menu, reduced-motion support
- **Layout patterns**: scroll-reveal animations, card-based repo display

## Decisions, constraints & rationale

- Single self-contained `index.html` file — must run in online compilers and browsers without a build step
- Three.js loaded via CDN using import maps
- GitHub repos fetched live from GitHub API with static fallback if API fails (online compiler compatibility)
- Single-code-file constraint drives all architecture choices

## Open questions & assumptions

- GitHub username/repo list not explicitly confirmed in this turn (data was fetched live)
- Exact repo descriptions inferred/filled in from API data
- 3D car model is a procedural primitive, not a loaded GLB asset (kept inline for single-file constraint)