# Linguly, Language Learning Platform

Linguly is an **open-source** language learning platform to serve a variety of language learning methods as a core architecture, focusing on transparency and flexibility.
It is providing the ground to easily switch between different methods and use them with a continuous experience.

## Why?

*What are the problems we want to solve here?*

### Learning continuity while still be able to change and improve tools and logics

With the rapid improvement in language models and AI, a lot of language learning possibilities have been unlocked.
We believe that the way we were traditionally learning language has been changed, and new methods can be improved in different ways.
Still finding an optimum tool to be the best language learning companion is not easy, and it might be different for each individual.
Therefore, a flexible platform to configure and try different methods can help us easily develop and experiment with new methods.
To tackle the issue thoroughly, this platform should have:

- Flexible Interfaces (Interaction methodology)
- Flexible Agents (method's logic)
- Flexible Language Model Access

These three flexibilities combined with a [Shared Context](#shared-context) concept will still ensure a continuous learning experience while improving the learning tools and methods over time.

### Transparency and control over personal data 

By growing AI-based tools, one of the biggest concerns of the users is how their data might be used for unintended purposes or learning other AI apps.
In Linguly, we are trying to address this concern by following:

- Linguly is open source, and it brings transparency to how we process and store data.
- We are documenting and supporting self-hosting Linguly, fully or partially, so you can easily host and manage your data.
- From the beginning, we are planning to provide easy ways of extracting your data and moving to any other self-hosted instance and continue your learning journey wherever you want.

## What?

Based on the three flexibility idea, we have defined the initial architecture as following:

### Architecture overview

![Linguly Architecture Overview](./linguly_architecture_overview.svg)

### Linguly Core

[Linguly Core](https://github.com/Linguly/linguly-core) is the central place to shape the platform.
It contains the [Agents](#agents) which are configurable using YAML files.
Agents' capabilities are limited to the definition of each type which can be extended by the [contributors](#how-to-contribute).  

### Agents

Agents are our language learning methodology logic. In each Agent we can define:

 - which [interfaces](#interfaces) can be connected
 - which [models](#models) to be used
 - what data to be stored and what to be read from the [shared context](#shared-context)
 - how to interact with the user

We can define and extend Agent's type and categories by developing them.
However, each Agent is an instance of those types which has been configured using the YAML files.
In this way, we can make them easily configurable and extendable by any user.
> **NOTE**: Initially we need a PR and redeployment for each new YAML file but later when we introduce the `Linguly Lab`, those can be configured via a separate interface.

### Interfaces

Interfaces are not only the provision of Agents in different devices and entry points, but also making experimenting/experiencing different interaction methodologies possible.
Not all interfaces will be able to serve all Agents' capabilities and vice versa. But they all should provide these basic functionalities:

- user login (it can also be through a link to a central login service)
- showing the list of available Agents for the interface
- switch between agents
- link to this page to get to know other interfaces and options :)

#### Currently available interfaces

- [Telegram Interface](https://github.com/Linguly/telegram-interface)
   - [Linguly Live](#linguly-live) instance: (Beta version) [@linguly_live_bot](https://t.me/linguly_live_bot)

### Models

Agents should have access to different language models based on their capabilities.
These models might be hosted open source models or a connection to the external models.
The 'Model Proxy' will manage the connection and interaction with different models.

### Shared Context

Shared Context is a set of information shared between Linguly Agents to recognize a user's [language state](#language-state) and [learning goals](#learning-goal) in order to adjust the learning experience accordingly.
> The `DB Proxy` pictured in the architecture will be the connector switch to enable us trying different types/instances of Dbs.
> **NOTE**: Shared Context is a core concept in Linguly. Using Shared Context we should be able to change Agents and learning logic but still continue our learning journey without interruption.

#### Learning goal

To begin a learning journey you can define a goal.
Interfaces should allow you to switch between goals and act accordingly to serve the new goal.

Each goal may include:

- Language
- Language type (for business, for study, ...)
- Language level
- Deadline (optional, not supported initially)

#### Language state

Here we try collecting information to tell agents what is your current level/progress according to your previous interactions with any agent.
It can include user manual input as well.

State may include:

- Current Language Level (manual input)
- Language Proficiency test result (from test Agents)
- Words/Statements state
- Grammar state (optional)
- Language mental model (in a knowledge graph or neural network): ultimate goal (advanced)

### Linguly Live

For each interface, we are hosting a free version to be used by the community. These instances has named as Linguly Live.
If you want to host a private instance to own your data you can follow the instructions in each repo and deploy them (We will later provide a central step by step guide).

### Linguly Lab

Linguly Lab will be the additional pillar on Linguly Core to manage the Agents configurations, Model connections, and interfaces to freely define new experiences.
It will be a powerful tool to provide a no code experience of configuring learning logic and provide it in specific interfaces.
Some of the benefits:

- **Academic Projects**: to modify and compare result of different methods
- **Admins**: to change and improve learning experiences available in Linguly Live
- **Learners**: to personalize and modify the Agents based on their needs plus sharing them with others

## How?

Linguly is an open-source project so it requires passionate people who share the same goal.
We want to work together to build a solution that will benefit the society and people to be empowered and learn new languages efficiently.

We want to shape a core team of main contributors to plan the project and manage its daily requirements.
Please feel free to [contact](#contact-us) if you are interested to join.

In addition, Linguly is open to everyone to [contribute](#how-to-contribute) and help us grow together.

### University alliances

This project has designed in a way to be suitable for variety of academic projects and experiments in language learning area.
So if you found it useful for your project, feel free to [contact](#contact-us).
We will be super happy to support and collaborate.

### How to contribute?

If you wish for a feature or change, have same passion and want to help, or just want to learn and try something, feel free to:

- [contact us](#contact-us)
- create a new issue
- pick an issue and start working on it

### How to support financially?

Currently, we are covering the basic costs ourselves with **no donation option**. However, we might set up donation options when the project grows to a certain level. 
So if you want to support us now:

- talk about this project with your friends and colleagues
- use it and give us feedback
- share your experience in social media
- contribute in the development!

## Contact Us

- Send an email to: linguly.contact@gamil.com
- Start a [discussion](https://github.com/orgs/Linguly/discussions)
