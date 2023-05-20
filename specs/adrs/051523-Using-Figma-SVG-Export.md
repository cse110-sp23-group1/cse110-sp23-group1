---
title: Using Figma SVG Export
status: accepted
date: 2023-05-15
deciders: Full Team
consulted: Full Team
informed: Full Team
---
# Use of SVG for Origami Visual

## Context and Problem Statement

Since we decided to use stop motion, we needed to decide how to represent the visual of the origami. This is not immediately obvious, since other functional needs (such as the operation of the paper, the flaps holding text) made the file format pretty important. In addition, there are pros and cons to other solutions, however, some solutions may require a more heavy implementation, others may require new resources, and some may require knowledge of a certain tool that not a majority of the team posses.

## Decision Drivers

* The user should be able to click on the flap they want to open
* The possibility of customizing the image would be nice
* Scalability of the image
* Each part of the fortune teller is clickable. The image itself should be fairly interactive.

## Considered Options

* PNG from figma. 
* SVG from figma.
* PNG from AI generation (Stable Diffusion, MidJourney).

## Decision Outcome

Chosen option: "SVG from figma", because it addresses all of the drivers.

### Consequences

* Good, because it paths in SVG can be treated as elements for events and its properties readily customized with loss of quality due to vector.
* Good, because Figma has a base CSS we can use later on to help touch up our SVG.
* Bad, because it will be hard/impossible to achieve a very unique visual representation (such as an artistic rendering, etc) with vector art
* Bad, because this kind of implementation is still difficult and time-heavy.

## Validation

This decision was discussed and agreed upon by the whole team at the beginning of our Week 7 Sprint.