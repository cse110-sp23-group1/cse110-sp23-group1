---
title: Functionality of Animating Fortune Teller
status: accepted
date: 2023-05-29
deciders: Full Team
consulted: Full Team
informed: Full Team
---
# Functionality of Animating Fortune Teller

## Context and Problem Statement

When the user first enters the page, they will be presented with the sidebar and the fortune teller. After choosing to or not to edit the fortunes, they will click on a flap they want to use first. Will this flap start the animation or will they have to click the flap and then click another button to start the animation? How will they know what to do?

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* User should understand how to operate the fortune teller.
* Intuitively, what would a user expect our product to do?
* Minimize the number of clicks it takes to start the fortune teller.
* Starting animation after flap click already implemented.

## Considered Options

* Start animation directly after clicking on a flap
    - Give user instructions on how to operate.
    - Let them figure out operation.
* Start animation after user clicks animate button. They would click on a flap first, then the button.
* A third option.

## Decision Outcome

Chosen option: To start the animation directly after clicking a flap because that would be the most intuitive way to the user. Also, this functionality was already implemented and would remove the work to add a button and its CSS and JS which would require more time.

### Consequences

* Good, because it requires less coding for the developers.
* Good, because it will require less clicks for the user to start the actual process of the fortune teller.
* Bad, because we may now need to include instructions or step-by-step to the user so they understand how to operate the fortune teller.
    - May require another ADR.

## Validation

This decision was discussion in #week-9-sprint in Slack and officially voted on in #general in Slack. Decision was agreed upon by full team in the poll.
