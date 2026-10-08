# CASTAWAY Alpha

CASTAWAY is a Survivor-inspired social survival life simulation. Its north star is a season inhabited by believable people with physical needs, relationships, incomplete information, memories, and consequences; the player is one castaway in that world.

**Start with [CASTAWAY_MAIN_TRUNK_CANON.html](CASTAWAY_ALPHA/CASTAWAY_MAIN_TRUNK_CANON.html). This is the primary, authoritative Alpha build surface in this repository.**

## Repository map

| File | Role |
| --- | --- |
| [CASTAWAY_MAIN_TRUNK_CANON.html](CASTAWAY_ALPHA/CASTAWAY_MAIN_TRUNK_CANON.html) | Canonical game trunk. Start here to explore the current Alpha or make campaign changes. |
| [CASTAWAY_APPROVED_CHALLENGE_LAB_V1.html](CASTAWAY_ALPHA/CASTAWAY_APPROVED_CHALLENGE_LAB_V1.html) | Separate challenge lab build for exploring and developing challenge interactions. Its filename does not establish that every lab behavior is integrated into the trunk. |
| [CASTAWAY_NARRATIVE_NORTH_STAR_DOSSIER.md](CASTAWAY_ALPHA/CASTAWAY_NARRATIVE_NORTH_STAR_DOSSIER.md) | Canonical product vision, simulation philosophy, and development guardrails. It describes what CASTAWAY should become; it is not a build-specific feature checklist or completion report. |

## Open the Alpha

1. Clone or download this repository.
2. Open `CASTAWAY_ALPHA/CASTAWAY_MAIN_TRUNK_CANON.html` in a browser.
3. Open the challenge lab separately when working on challenge interactions.

The repository contains two HTML builds and the Markdown dossier; it does not include a package-manager setup or a separate compilation workflow. GitHub's file view displays source rather than running the game.

If your browser restricts local-file behavior, serve the repository with a local static server. For example, with Python 3 installed, run this from the repository root:

```sh
python3 -m http.server 8000
```

Then visit [the main trunk locally](http://localhost:8000/CASTAWAY_ALPHA/CASTAWAY_MAIN_TRUNK_CANON.html). Keep the same browser and address when returning to a saved campaign.

## Current Alpha scope

The checked-in trunk is a browser-based development build with code and UI for campaign setup and Pregame, camp and time progression, castaway physical and social state, challenges, Tribal and endgame systems, and local save slots. The separate lab provides a challenge-focused development surface.

These are areas represented in the source, not a claim that every path is complete, balanced, or verified through an uninterrupted season. Use the trunk to establish actual current behavior and the dossier to evaluate intended behavior.

The design priorities are spatial and time continuity, separate world truth/player knowledge/NPC beliefs, NPC autonomy, persistent consequences, and emergent stories. Features should preserve those principles as the Alpha grows.

## Known limitations and status boundaries

- **Alpha maturity:** This is an evolving development snapshot. Full-season reliability, balance, performance, and device/input compatibility are not established by this README.
- **Vision versus implementation:** Dossier goals and historical development notes do not prove that a feature is currently implemented or complete. Verify each feature in the canonical trunk before describing it as shipped.
- **Lab versus trunk:** Challenge-lab behavior must be checked for campaign integration, state safety, cleanup, and inputs before being treated as canonical game behavior.
- **Browser saves:** The builds use browser local storage. Saves depend on the browser and origin; clearing site data or changing how the build is opened can make prior saves unavailable. Cross-build save compatibility is not guaranteed here.
- **Validation:** This snapshot contains no separate automated test suite or CI configuration. Source inspection alone does not establish runtime correctness.
- **Version labels:** Embedded titles and historical comments differ between builds. Use the canonical filename and Git commit to identify the build being discussed rather than assuming the largest embedded version number determines authority.

## Working on CASTAWAY

Read the dossier before substantial design changes. Make campaign changes against the canonical trunk and treat the lab as a separate development surface.

For a change or bug report, identify the file and commit, browser/device, reproduction steps, and expected versus observed behavior. Follow the dossier's testing cadence: targeted regression checks and a short trunk smoke test for each feature, with broader audits at major milestones.
