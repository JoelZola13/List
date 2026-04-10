# Communication App Brief

This repository starts from the upstream [listmonk](https://listmonk.app/) codebase and serves as the foundation for a broader communication platform.

## Product direction

The initial framework already gives us:

- subscriber and list management
- campaigns and templates
- analytics
- transactional messaging hooks
- API coverage and extensibility points

Our app can build on that base to become a multi-channel communication platform instead of only a newsletter tool.

## Working assumption

Until we define the product in more detail, we will treat Listmonk as the core messaging engine and extend around it rather than rewriting its internals early.

That means we should prefer:

- custom workflows before deep forks
- API-driven integrations before schema changes
- additive UI features before disruptive admin rewrites

## Suggested architecture layers

1. Core messaging engine: upstream Listmonk backend, frontend, database, and campaign logic.
2. App-specific domain layer: communication journeys, audience rules, organization-specific workflows, approvals, or automation rules.
3. Channel extensions: email first, then optional SMS, WhatsApp, push, or webhook-based delivery through messenger integrations.
4. Experience layer: branded admin experiences, dashboards, and app flows specific to this project.

## First milestone

The best first build target is to get a local dev environment running and then choose one focused customization slice.

Recommended first slice options:

- branded admin customization
- custom audience segmentation workflow
- transactional messaging API wrapper
- multi-channel message orchestration concept

## Repo workflow

- keep upstream framework behavior intact unless we are intentionally changing it
- document product decisions before broad refactors
- make small vertical slices that can be tested locally

## Immediate next step

Use the local setup guide in [START_HERE.md](./START_HERE.md) to boot the app, then pick the first feature slice we want to implement.
