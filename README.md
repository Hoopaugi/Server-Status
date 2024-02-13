# Server Status

Dashboard to show server status information

## Before pushing:

Lint and fix any problems

    npm run lint

To merge all workflows have to pass

## Setup

Install backend dependencies. Inside `services/backend` run

    npm install

Start in development mode

    docker compose up

## Stack

- Express backend
- Vue.js frontend
- MongoDB as the database
- Each service running as a docker container
- nginx to route traffic
- Typescript used at least for the backend
- Github Actions for CI/CD

## Notes

- Repository main branch is protected. Checks must pass for a merge
- Backend currently developed using latest node. Needs to be locked down in the future
