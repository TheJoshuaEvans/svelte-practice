# Svelte Practice IAC
This directory contains infrastructure as code for the `svelte-practice` project. This includes CDK scripts for deploying cloud infrastructure on AWS, as well as a complete docker environment

## Commands
The following commands are supported
Command | Description
--------|-----------
`docker:up` | Initialize the docker environment
`docker:down` | Destroy the docker environment and all related resources
`attach:frontend` | Attach to a running frontend docker instance
