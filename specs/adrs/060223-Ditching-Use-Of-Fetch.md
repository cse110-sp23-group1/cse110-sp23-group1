---
title: Ditching Use of Fetch
status: accepted
date: 2023-06-02
deciders: Full Team
consulted: Full Team
informed: Full Team
---
# Ditching Use of Fetch

## Context and Problem Statement

When the user enters our site, they are presented with 8 preset fortunes. They can changea any of these fortunes. The problem with is how we want to fetch these fortunes from our own storage. Should we use a JSON file, put them in JavaScript, create a fetch function to grab them from somewhere?

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* Network Overhead
* Over implementation
* Time Constraint (only 1 week left)

## Considered Options

* Hard coding an array into the Origami.js file
* Putting default fortunes into a separate JSON file and using fetch() to fetch them.
* Putting default fortunes into a seperate JS file and using import to get them.

## Decision Outcome

Chosen option: Putting default fortunes into a seperate JS file and using import to get them. This decision was the best option as it keeps our Origami.js file cleaner as well as keeps everything local first. The implementation is far easier and does not require any network overhead. The fortunes will always be loaded in when the user enters the site since the defaults are local.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because keeps a local first mentality.
* Good, because requires no network overhead.
* Good, because it is very easy to implement.
* Good, because still able to add different languages.
* Bad, beacuse we have already spent over 2 weeks on fetch(), however, fetch() doesn't work when running on Github Pages, so a bit of time wasted.

<!-- This is an optional element. Feel free to remove. -->
## Validation

This decision was discussion in #week-9-sprint in Slack and officially voted on in #general in Slack. Decision was agreed upon by full team in the poll.

<!-- This is an optional element. Feel free to remove. -->
## Pros and Cons of the Options

### Hard Coding into Origami.js

* Good, for all reasons with accepted option, however, may make code less clean.

### Fetching JSON

* Bad, because requires network overhead.
* Bad, because did not work on Github pages server.
* Bad, because difficult to implement.
* Bad, because when fortunes failed to load, user would have to input 8 of their own.

<!-- This is an optional element. Feel free to remove. -->
## More Information

[Click Here](https://v8.dev/blog/cost-of-javascript-2019#json) for a link to see some evidence for this decision.
This blog post stated that `A good rule of thumb is to apply this technique for objects of 10 kB or larger` which we will never reach since we currently only have English default fortunes. Thus, based off this evidence, we made the correct decision.

[Click Here](https://stackoverflow.com/questions/59149074/apparently-json-parse-is-faster-than-declaring-an-object-literal-if-thats-the) for more evidence about how we should be going about our problem.
