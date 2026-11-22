# Mac Utility Kit

**Build the foundation once. Create useful Mac apps again and again.**

Mac Utility Kit is a **new** open-source SwiftUI starter for native macOS menu bar utilities, planned for **Kiroween 2026 / Skeleton Crew**. The aim is to prove that one genuinely reusable foundation can support two distinct, working apps.

**Status:** initial project planning scaffold only. No apps or shared package have been implemented yet.

## Planned demonstrations

| App | Main job | Implementation status |
| --- | --- | --- |
| **CleanPaste** | Normalize clipboard text (strip rich-text formatting, trim whitespace, fix line breaks), preview and copy | Planned |
| **FocusTick** | A focused menu bar timer (start, pause, reset, optional notifications) | Planned |

The two apps must have **separate app folders and targets** and depend on one common Swift Package. Unique business logic belongs in each app, not in the shared package.

## Repository structure

```
.kiro/steering/             # Goals, architecture, and coding constraints for Kiro
Foundation/MacUtilityKit/  # Shared Swift Package, to be built with Kiro Crew
Apps/CleanPaste/            # First standalone macOS app, to be built with Kiro Crew
Apps/FocusTick/             # Second standalone macOS app, to be built with Kiro Crew
```

## Development approach

Use **Kiro Crew** as the primary development environment. First specify shared needs, then implement and test the Swift Package, build each app on it, and validate both apps independently. Keep a record of actual Kiro usage and decisions; do not claim tools or features that have not been used.

### Suggested acceptance criteria

- [ ] `Foundation/MacUtilityKit` is a reusable Swift Package; both apps import it.
- [ ] Both apps build and launch independently on a supported version of macOS.
- [ ] CleanPaste can transform sample clipboard text, preview before/after, and copy the result.
- [ ] FocusTick can start, pause, and reset a timer from its menu bar UI.
- [ ] Settings and menu bar UI primitives are genuinely shared, not duplicated.
- [ ] Automated tests cover shared components and core transformations/timer state.
- [ ] GitHub repository is public, has an open-source license, and includes `.kiro` at the root.
- [ ] README lists build/test commands and links to working builds when available.
- [ ] Demo video (up to 3 minutes) shows both apps, shared Swift package, and actual Kiro workflow.

## Background

The motivation comes from years of macOS application work at [MacPlus Software](https://noteifyapp.com/apps/). Existing applications are **inspiration only**, not part of this new contest entry. Disclose any pre-existing source code if it is later incorporated.

## License

MIT; see [LICENSE](LICENSE).
