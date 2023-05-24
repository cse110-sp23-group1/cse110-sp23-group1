---
title: Clicking Out of Input Fortune Box
status: accepted
date: 2023-05-23
deciders: Full Team
consulted: Full Team
informed: Full Team
---
# Clicking Out of Input Fortune Box

## Context and Problem Statement

Problem: When a user clicks on an element in the sidebar to open the input fortune box, clicking outside of the box should have behavior. However, there are many different options for what this is. For the user, what is the most intuitive and convenient behavior for when the user clicks outside the input box? 

## Decision Drivers

* Users who have seen similar features in other apps expect certain responses. 
* Intuitively, what would make sense to a user who has never seen such a feature. 
* Other options within the app that the user has to get the same behavior

## Considered Options

* The input box closes and user's input is saved 
* The input box closes and user's input is not saved
* Nothing happens

## Decision Outcome

Chosen option: The input box closes and user's input is not saved. It is also intuitive to save the user's input only when they explicitly indicate their intention, such as by clicking the save button or pressing the "enter" key. This approach is consistent with how many other applications handle input interactions. Most other applications also behave like this. For example, in video games, typing a message inside chat boxes and clicking outside the box typically does not send your message. By adopting a similar approach, a familiar and user-friendly experience is maintained. 

### Consequences

* Good, because it is intuitive to use. 
* Good, because users who use other similar apps will have an easy time adapting to this one. 
* Bad, because it is easy for the user to accidentally click outside of the box and lose progress on their customized fortune. 

## Validation

This decision was discussed and agreed upon by the whole team in a poll in #general in Slack. 
