# Svelte Practice
Just practicing using Svelte, working through the tutorial as well as some bonus bits

Things to do:
- [ ] Go through Svelte tutorial
- [ ] Implement IAC stuff using CDK
- [ ] Set up local docker environment

## Project Structure
This project is split into ~~three~~ two directories [frontend](frontend) and [iac](iac). A backend directory would also exist if this project had any backend components (and it will eventually, I just don't feel like diving into LocalStack right now)

### Frontend Directory
This directory holds the actual Svelte app and all files that will find there way into a user's browser. It is based off of the [Svelte template](https://github.com/sveltejs/template) and follows that general file structure

### IAC Directory
This directory handles infrastructure as code, as implemented by [AWS CDK](https://aws.amazon.com/cdk/), as well as docker configurations for local development (or... it will eventually at any rate)
