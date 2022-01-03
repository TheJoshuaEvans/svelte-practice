# Svelte Practice
Just practicing using Svelte, working through the tutorial as well as some bonus bits. This is meant to act as a resource that I can refer to later when building real Svelte apps and be a foundation for a Svelte project template

Things to do:
- [ ] Go through Svelte tutorial
  - [X] Introduction
  - [X] Reactivity
  - [X] Props
  - [X] Logic
  - [X] Events
  - [ ] Bindings
  - [ ] Lifecycle
  - [ ] Stores
  - [ ] Motion
  - [ ] Transitions
  - [ ] Animations
  - [ ] Actions
  - [ ] Classes
  - [ ] Component composition
  - [ ] Context API
  - [ ] Special elements
  - [ ] Module context
  - [ ] Debugging
- [ ] Implement IAC stuff using CDK
- [X] Set up local docker environment
- [X] Set up ESLint

## Project Structure
This project is split into ~~three~~ two directories [frontend](frontend) and [iac](iac). A backend directory would also exist if this project had any backend components (and it will eventually, I just don't feel like diving into LocalStack right now)

### Frontend Directory
This directory holds the actual Svelte app and all files that will find there way into a user's browser. It is based off of the [Svelte template](https://github.com/sveltejs/template) and follows that general file structure

### IAC Directory
This directory handles infrastructure as code, as implemented by [AWS CDK](https://aws.amazon.com/cdk/) (eventually), as well as docker configurations for local development
