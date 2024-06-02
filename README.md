# Ansible playbook for Libre Chat

## Description

This project contains an Ansible playbook for setting up and managing Libre Chat. The playbook is designed to be run in
a Docker container for isolation and reproducibility.

The playbook uses a Taskfile for task running and management. The Taskfile contains tasks for setting up the
environment, running the deploy container, stopping the deploy container, linting, and running the playbook.

Environment variables are managed through a `.env` file, which includes settings for SSH, OpenAI, VectorDB, and MongoDB.
These variables are used in the Taskfile and the Ansible playbook.

Before running the playbook, you need to set your variables in the `.env` file and create
a `configuration/private_key.pem` file with your private key. After these steps, you can run the playbook
using `taskfile run`.

## Prerequisites

1. Installed "[TaskFile](https://taskfile.dev/installation/)"

## Steps

1. Copy `./env.example` to `./.env`
2. Set your variables in `./.env`
3. Create `configuration/private_key.pem` file and copy your private key into it
4. Copy `users.example.yaml` to `.users.yaml` and set your users for the chat 
5. Run `taskfile run` to run the playbook
