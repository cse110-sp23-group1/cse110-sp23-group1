---
title: Input Preset Text Should Be Current Fortune
status: accepted
date: 2023-05-17
deciders: Full Team
consulted: Full Team
informed: Full Team
---
# Input Preset Text as Current Fortune

## Context and Problem Statement

Currently, a user will be given 8 boxes on a sidebar, such that each box has a preset input. However, a user can click on a box and change the input so that when they run the fortune teller, they can have one of their inputs be one of the possible fortunes in the end. Problem is simply deciding what method would be best for the user when they try to change the input presets. Should the textbox they click to change the input show an empty preset, a preset of the old edit they made, a preset of the current fortune, or something else?

## Decision Drivers

* User should be certain of which input they are changing.
* Intuitively, what would make the most sense.
* Many other programs with presets would show you the current thing you are editing.

## Considered Options

* Empty Preset
* Preset of the Most Recent Edit
* Preset of Current Fortune

## Decision Outcome

Chosen option: Preset of current fortune was chosen because intuitively, it would make the most sense. When you normally go back to edit some text, for example, a document or a username or password, the text remains the same and you edit on it, therefore, it would not make sense to have an empty preset. Putting the preset of the most recent edit would confuse the user about which fortune they are editing, thus, it would make the most sense to use the preset of current fortune.

### Consequences

* Good, because user will know which fortune they are editing.
* Good, because user will be used to this kind of preset since that is what other programs across the web do.
* Bad, because implementation might become a little more complicated.

## Validation

This decision was discussed and agreed upon by the whole team in #future-110-project in Slack. Majority (basically unanimous) votes asked to have the preset be of the current fortune.