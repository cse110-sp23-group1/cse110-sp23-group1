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
# Decision to Stat Local-First

## Context and Problem Statement

{Describe the context and problem statement, e.g., in free form using two to three sentences or in the form of an illustrative story.
 You may want to articulate the problem in form of a question and add links to collaboration boards or issue management systems.}
 The team was faced with the option of using a live-updating, LLM based API as part of our fortune teller, in order to create a more 
 dynamic and personalized response for the user. While this sounds like a desireable feature to have, we decided to stick to 
 preset responses that the user can edit, making it such that we do not depend on any API to have predictions for the user. Our reason
 for doing this is that in general, integrating an API allows more room for error, and failed get requests. Furthermore, LLM have lots
 of room for error, and catching these errors in real time would be important and difficult to implement given our timeline.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* Time Constraints: Any feature we consider including must fit our relatively short timeline. After consdering our number of weeks*team members*expected hours devoted to this project per week, it did not seem feasible to implement
* Deterministic Output: LLM's are inherently non-deterministic in their outputs. While this allows for personalization, it adds a greater need for testing that does not seem worth it for the feature

## Considered Options

* Keep a fully local-first approach and completely exlude any LLM based API's. User can input their out custom outputs.
* Try to implement the feature using an LLM based API and have a backup set of locally stored responses if something goes wrong
* Try to implement the feature using an LLM based API and try to catch and retry unexpected/undesired outputs
* … <!-- numbers of options can vary -->

## Decision Outcome

Chosen option: Keep a fully local-first approach and completely exlude any LLM based API's, because
its more important for us to establish a basic product within a timeline, and leave "nice to have" features
if we finish early.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because we have a more straight-forward design, implementation, and testing process
* Bad, because we cannot automatically give user a more creatice output, they must input it themselves.
* … <!-- numbers of consequences can vary -->

<!-- This is an optional element. Feel free to remove. -->
## Validation

This decision was discussed and agreed upon by the whole team in our planning phase.
