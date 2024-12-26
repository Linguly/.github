# Linguly, Language Learning Platform

Linguly is a language learning platform to serve different methods of language learning as a core architecture. It is providing the ground to easily switch between different methods and use them 

## Why?

*What is the problem we want to solve here?*

With the rapid improvement in language models and AI, a lot of language learning possibilities have been unlocked.
We believe that the way we were traditionally learning language has been changed and new methods can be improved in different ways.
Still finding an optimum tool to be best language learning companion is not easy and it might be different for each individual.
Therefore, a flexible platform to configure and try different methods can help us easily developing and experimenting new methods.
To tackle the issue thoroughly, this platform should have:

- flexible Interfaces (Interaction methodology)
- flexible Agents (Method's logic)
- flexible Language Model Access

## What?

Based on these three flexibility idea, we have defined the initial architecture as following:

### Architecture Overview

![Linguly Architecture Overview](../linguly_architecture_overview.svg)

### Linguly Core

[Linguly Core](https://github.com/Linguly/linguly-core) is the central place to shape the platform. It contains the [Agents](https://github.com/Linguly#agents) which are configurable using YAML files.
Agents' capabilities are limited to the definition of each type which can be extended by the [contributors](https://github.com/Linguly#how-to-contribute).  

### Agents

Agents are our language learning methodology logic. In each Agent we can define:

 - which [interfaces](https://github.com/Linguly#interfaces) can be connected
 - which [models](https://github.com/Linguly#models) to be used
 - what data to store and what to read from the [shared context](https://github.com/Linguly#shared-context)
 - how to interact with the user

We can define and extend Agent's type and categories by developing them.
However, each Agent is a variety of those types which has been configured using the YAML files.
In this way, we can make them easily configurable and extendable by any user.
> **NOTE**: Initially we need a PR and redeployment for each new YAML file but later when we introduce the `Linguly Lab`, those can be configured via a separate interface.

### Interfaces

Interfaces are not only the provision of Agents in different devices and entry points, but also making experimenting/experiencing different interaction methodologies possible.
Not all interfaces will be able to serve all Agents' capabilities and vice versa. But they all should provide these basic functionalities:

- user login
- showing the list of available Agents for the interface
- switch between interfaces
- link to this page to get to know other interfaces and options :)

#### Current Interfaces

- [Telegram Interface](https://github.com/Linguly/telegram-interface)
   - No live instance yet

### Models

Agents should have access to different language models based on their capabilities.
These models might be hosted open source models are a connection to the external models.
The 'Model Proxy' will manage the connection and interaction with different models.

### Shared Context

Shared Context is a set of information shared between Linguly Agents to recognize a user's language state and goals and adjust the learning accordingly.
> The `DB Proxy` pictured in the architecture will be the connector switch to enable us trying different types/instances of Dbs. However, in the initial implementation it will be simplified.

#### Learning Goal

To begin a learning journey you can define a goal.
Interfaces should allow you to switch between goals and act accordingly to serve the new goal
Each goal can include:

- Language
- Language type (for business, for study, ...)
- Language level
- Deadline (optional, not supported initially)

#### Language State

Here we try collecting information to tell agents what is your current level/progress according to your previous interactions with any agent.
It can include user manual input as well.
These may include:

- Current Language Level (manual input)
- Language Proficiency test result (from test Agents)
- Words/Statements state
- grammar state (optional)

### Linguly Live

For each interface, we are hosting a free version to be used by the community. These instances has named as Linguly Live.
If you want to host private instance to own your data you can follow the instructions in each repo and deploy them.

## How?

Linguly is an open-source project so it requires passionate people who share same goal. We want to work together to build a solution that will benefit the society and people to be empowered and learn languages efficiently.

There would be a core team of main contributors to plan the project and manage its daily requirements. However, it is open to everyone to [contribute](https://github.com/Linguly#how-to-contribute) and help us grow together.

### University Alliances

This project has designed in a way to be suitable for variety of academic projects and experiments in language learning area. So if you feel it can possibly help you too, feel free to contact. We will be super happy to support and collaborate.

### How to contribute?

If you wish for a feature or change, have same passion and want to help, or just want to learn and try something, feel free to:

- [contact us](https://github.com/Linguly#contact-us)
- create a new issue
- pick an issue and start working on it

### How to support financially?

Currently, we are covering the basic costs ourselves with **no donation option**. However, we might set up donation options when the project grows to a certain level. 
So if you want to support us:

- talk about this project with your friends and colleagues
- use it and give us feedback
- share your experience in social media
- contribute in the development!

## Contact Us

- Send an email to: linguly.contact@gamil.com
- Start a [discussion](https://github.com/orgs/Linguly/discussions) 
