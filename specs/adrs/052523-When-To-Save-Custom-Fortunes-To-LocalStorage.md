---
title: When To Save Custom Fortunes To LocalStorage 
status: accepted 
date: 2023-05-25
deciders: Full Team
consulted: Full Team
informed: Full Team
---
# When To Save Custom Fortunes To LocalStorage

## Context and Problem Statement

We currently have a fortune teller with 8 preset fortunes. However, users, can edit these fortunes to their likings. When they edit these fortunes, we have decided to save them to localStorage, but the problem is not knowing if its better to save them when the user is done editing all of them and hits the play button or as they edit each fortune individually.

## Decision Drivers

* Editing them on play could lose the fortune they edited if they never clicked play.
* Simply saving everything to localStorage on play is an easier implementation.
* User should have their fortunes save if they ever come back to the site.
## Considered Options

* Save on play, after editing whatever they wanted.
* Save on fortune load/change.

## Decision Outcome

Chosen option: Saving on the custom fortune changing or loading was the better decision. It makes more sense for the user's change to be saved as they make such a change. If the user were to change a couple fortunes, leave the site, then come back, those changes would be saved. The other option would be easier for us, the developers, but not so great for the user/client side.
### Consequences

* Good, because user will now have their custom fortunes constantly saved.
* Bad, because implementation became a little bit more work.

## Validation

This decision was discussion and agreed upon by the whole team during the weekly meeting and in the sprint channel in Slack.
