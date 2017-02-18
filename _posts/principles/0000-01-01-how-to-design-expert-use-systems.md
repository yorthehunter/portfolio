---
layout: post
title: Designing Expert Use Systems
permalink: /how-to-design-expert-use-systems/
categories: principles
nav: principles
max-width: md
---

1. LEARN FROM YOUR USERS AND BUSINESS PARTNERS.
    * We get in front of our users as soon as we can and we never stop learning from them.
    * But sometimes it's okay to file feedback into the "later" bin; we have to be able to react thoughtfully.

1. Design for high information density
    * The fastest interaction is just moving your eyeballs
	* Use all of the screen real estate
    * Our users value efficiency over readability in most cases
    * Many business partners rely on laptops with small-ish screens.

1. High contrast visual design
	* Black text on white backgrounds is very high legibility.
	* Use legibility and color contrast tools to
    * We value legibility over aesthetics.
    * As designers we are more attuned to subtle nuances of color and contrast than our users are.

1. Our users are mostly big-screen and hands-off. We're not blindly mobile-first.
    * Build for our specific users' needs first.
    * We are not mobile-first; we are user-first.
    * Responsiveness mostly comes free with our framework. It's typically not necessary to spend a ton of time optimizing different breakpoints since our users are generally on laptop-to-desktop-sized screens.

1. Feedback, Undo, Prevent.
	* Err on the side of more rather than less freedom. We can't predict everything our customers will want to do with our software; err on the side of trust.
	* Expert users know what they're doing and need to be efficient. Let them take actions with a minimum of confirmations; provide feedback that an action has succeeded.
	* Design for "undo" whenever possible. If a user makes a huge mistake, provide a path for them to make the change that un-does it.
	* Prevent disastrous mistakes. Don't build a system that lets a user make a horrible mistake in the first place. Try approval paths, sandboxes, and confirmations.

1. Make error messages useful and descriptive.
	* What went wrong?
	* What do I need to do to fix it?

1. Fitts' law matters.
	* Reduce the number of gestures that it takes to complete repeated actions.
	* Radio buttons instead of dropdowns.
	* Keyboard shortcuts.
	* Audio feedback – so the user's eyes can be moving to the next thing in the list instead of looking for a visual confirmation message.


1. Sometimes the best interaction is no interaction.
	* Prefill, guess, parse.
	* [Almost] always provide a default choice or action. Use data to learn about the most likely or more frequent cases and emphasize those.
	* Data filtering that fits the use-case and level of knowledge
    * Advanced filtering for experts, “fuzzy” searching, etc.


1. Innovation in interface design is rarely a virtue.
	* Be a fascist about sticking to the style guide.
    * When the convention exists, ***use it***
	* Optimize for standard patterns, clarity, and radical usabiltiy.
	* Innovate on our business processes and user experience, not by recreating solved design patterns.
	* Innovation is appropriate for new interaction styles, e.g. voice-controlled or hands-free, that may exist as a result of our particular business processes.
	* Follow standard conventions in all aspects of the UI, from language to visual design to interaction design and everywhere in-between. Chances are, someone has solved the problem to some degree.
