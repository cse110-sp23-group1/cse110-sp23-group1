---
# Configuration for the Jekyll template "Just the Docs"
parent: Decisions
nav_order: 100
title: ADR Template

# These are optional elements. Feel free to remove any of them.
# status: {proposed | rejected | accepted | deprecated | … | superseded by [ADR-0005](0005-example.md)}
# date: {YYYY-MM-DD when the decision was last updated}
# deciders: {list everyone involved in the decision}
# consulted: {list everyone whose opinions are sought (typically subject-matter experts); and with whom there is a two-way communication}
# informed: {list everyone who is kept up-to-date on progress; and with whom there is a one-way communication}
---
<!-- we need to disable MD025, because we use the different heading "ADR Template" in the homepage (see above) than it is foreseen in the template -->
<!-- markdownlint-disable-next-line MD025 -->
# Use of SVG for origami visual

## Context and Problem Statement

Since we decided to use stop motion, we needed to decide how to represent the visual of the origami. This is not immediately obvious, since other functional needs (such as the operation of the paper, the flaps holding text) made the file format pretty important.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* The user should be able to click on the flap they want to open
* The possibility of customizing the image would be nice
* Scalability of the image

## Considered Options

* PNG from figma. 
* SVG from figma.
* PNG from AI generation.

## Decision Outcome

Chosen option: "SVG from figma", because it addresses all of the drivers.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because it paths in SVG can be treated as elements for events and its properties readily customized with loss of quality due to vector.
* Bad, because it will be hard/impossible to achieve a very unique visual representation (such as an artistic rendering, etc) with vector art
* … <!-- numbers of consequences can vary -->
