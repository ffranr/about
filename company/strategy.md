# Sourcegraph master plan

Everything we do stems from our [purpose](#purpose), to help *everyone* build software. We'll accomplish that over the next 30 years by following our strategy:

- 30 years
  - [Purpose](#purpose)
  - [Mission](#mission)
  - [Values](#values)
- 10 years
  - [10-year vision](#10-year-vision)
  - [Big Code](#big-code)
- 3 years
  - [3-year vision](#3-year-vision)
  - [Principles](#principles)
  - [Assumptions](#assumptions)
- 1 year
  - [1-year vision](#1-year-vision)
  - [Product direction](#product-direction)
  - [OKRs](#okrs)

## Purpose

We want everyone to be able to build software. A world where everyone, not just the ~0.2% who can code today, builds software will see faster and more broadly beneficial technological progress.

### Background

Everyone, in every community, in every country, and in every industry—not just the ones working at the half-dozen dominant tech companies—should be able to create products using the best technology. We believe this is the only way the world will sustain broad economic growth and build the innovations we need over the next 100 years in transportation, health care, energy, AI, communication, space travel, etc.

In 1976, just 0.2% of the world's population had access to a computer.

Apple's vision then was to create a "bicycle for the mind" in the form of a computer, and Microsoft put a computer "on every desk and in every home."

Together, these companies succeeded in bringing computing to billions of people. But these billions of people are still using software applications built by just 0.2% of the world's population (those who can code).

The next step is to make it so billions of people, not just 0.2% of the world population, can build software (not just use it). Cloud infrastructure providers solve the distribution piece: a tiny team can reach millions of users using the same infrastructure available to the most advanced tech companies. But the process of creating software is stuck in the mainframe era: the developer experience of building software is still poor, duplicative, manual, and single-player—and every software project is about integrating components of variable quality developed mostly in isolation, with a high chance of failure.

If you think everyone building software will never happen, ask yourself: is coding more like reading and writing (which virtually everyone does) or publishing books (which ~0.2% of the population does)? We think it's more like reading and writing.

## Mission

To achieve our [purpose](#purpose), our mission is to make it so everyone can participate in building software that improves people's lives.

## [Values](values.md)

Our [values](values.md) are the principles we want to uphold as we work toward our mission.

## Big Code

[Big Code](https://thenewstack.io/universal-code-search-a-new-search-tech-for-the-era-of-big-code/) is the idea that the amount, complexity, and value of code is growing quickly.

This is both good and bad:

- Good: More software is getting built, which can improve people's lives.
- Good: Developers can build on top of an ever-greater supply of existing code/libraries.
- Bad: More code and more complexity cause developer productivity to sharply decline.

As more and more people start coding worldwide, Big Code will get even bigger.

We want to make Big Code a good thing, not a bad thing, by making code more discoverable, more valuable, and easier to understand.

## Vision

We've written down our vision for Sourcegraph 1, 3, and 10 years from now.

### 1-year vision {#1-year-vision}

> Problem statement: In large and complex codebases ([Big Code](#big-code)), it's hard for developers to discover, understand, and fix code.

Sourcegraph universal code search is the one place to find and fix things across all code.

- Sourcegraph knows most everything that can be known about your code (from the compiler, build systems, code hosts, runtime metrics, docs, issues, project management, etc.).
- It's easy to find and use this information on Sourcegraph itself and in your editor, code host, and code reviews.
- You use Sourcegraph in your existing workflows for writing, reviewing, understanding, and fixing code.

### 3-year vision {#3-year-vision}

> Problem statement: Developers spend too much time on repetitive and overhead tasks, not on writing code to solve unique business problems.

Sourcegraph understands higher-level software development patterns and manages processes in the background for you, which lets you spend more time on the higher-leverage tasks that truly require your human brain.

- Sourcegraph has support for codifying concepts such as code ownership, tests, deployment, logging, tracing, performance, monitoring, build processes, and APIs. How you implement these is up to you. (If you do something non-standard, you just need to teach Sourcegraph, for example, how to determine where a particular file's code is deployed.)
- Sourcegraph has purpose-built new workflows that build on these concepts for common tasks. For example, if an application is reported down by your monitoring service, the first step is to visit a Sourcegraph page that shows all relevant information (recent deployments, recent commits, aberrant traces and logs, code owners, etc.) and presents your organization's preferred actions (roll back, create war room chat channel, etc.).
- When you make a change to an API, you can include "metacode" that knows how to update all usages of the changed API. Sourcegraph will show you a compatibility report and propose those changes on all downstream callers along with your change.
- You can discover and more easily use libraries, with statistics about usage patterns and a code marketplace.

> Unlike the [1-year vision](#1-year-vision), our 3-year vision involves Sourcegraph modifying existing workflows and being proactive.

### 10-year vision {#10-year-vision}

> Problem statement: Software development is a black box to everyone else in an organization. Communication and collaboration in both directions is poor.

Everyone involved in the software value chain (developers, sales, product, marketing, support, customers/users, etc.) uses Sourcegraph to coordinate work and share information.

From a developer's point of view, they can go from the code for a particular feature to a list of all customers using it, all feedback and support requests about it, and all upcoming features that relate to it.

From a customer's and salesperson's point of view, they can see all in-progress or planned features for the particular customer. For any given feature, they can see the current state of development.

> Unlike the [3-year vision](#3-year-vision), our 10-year vision involves more kinds of people using Sourcegraph (not just people who write code directly).

## Principles

- Sourcegraph is universal code search, not universal "everything" search. Any additional data types in our search need to be relevant to the software development workflow.
- We're a mass-market company and must maintain broad appeal. We want every developer, not just a specific niche audience, to use Sourcegraph.
  - Any given developer will only pick one code search tool to use. Any given company will standardize on a single code search tool. Therefore, to avoid fragmentation, Sourcegraph should be not only *much* better than the alternatives, but also *not worse* in any significant way.
  - We won't adopt polarizing public stances that would divide our audience.
- Our product should strive to be fundamentally privacy-respecting and secure. This means that users don't need to trust us to verify that their data is private and secure.
- Build on-ramps in our product to turn more people into frequent users, instead of building the product *for* infrequent users (which is a self-fulfilling prophecy).
- We eventually want to be a platform that ties together all of the tools developers use.
  - Other developer tools are partners, not as competitors.
  - This entails designing more extensibility into our product (and documenting it more thoroughly) than what's needed today, in order to make it easy for other people to build on.

## Assumptions

- Sufficiently good code search will be useful to every developer many times per day (on average). It may take a while to convert any specific person into a frequent code search power user, but it will happen eventually.
- Code search that is *exclusively* for public/open-source code is not actually that useful because most people spend most of their time working on their organization's internal code.

## Pricing

- Trying Sourcegraph (to prove it works and is valuable) is free and (if you want) self-service.
- If your organization is getting value from Sourcegraph with a lot of users, our [pricing](https://about.sourcegraph.com/pricing) is designed so that we earn money from you. This lets us invest in improving our product.
- All users at a given customer are on the same pricing tier. This is simpler than having users at different tiers and encourages us to build things that are broadly valuable.

## [Product direction](../direction/index.md)

Our [product direction](../direction/index.md) describes what we plan to build to make this vision real.

## [OKRs (goals)](okrs/index.md) {#okrs}

Our [OKRs (goals)](okrs/index.md) describe what each of us is doing this quarter to work toward our mission.
