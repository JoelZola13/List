# Start Here

This repo is the upstream Listmonk framework plus project docs for our communication app.

## 1. Prerequisites

You will need:

- Go
- Node.js
- Yarn
- Docker Desktop or a local PostgreSQL instance

## 2. Fastest local startup path

For the smoothest first run, use the provided Docker-based dev stack.

### Build and initialize the local dev database

```bash
make init-dev-docker
```

### Start the local frontend and backend

```bash
make dev-docker
```

Then open:

- `http://localhost:8080` for the frontend dev app

## 3. Alternative local workflow

If you want to run the backend and frontend directly on your machine instead of inside containers:

1. Copy `config.toml.sample` to `config.toml`.
2. Update the PostgreSQL settings in `config.toml`.
3. Build the app with `make dist`.
4. Install the database with `./listmonk --install`.
5. Run the backend with `make run`.
6. In another terminal, run the frontend with `make run-frontend`.

## 4. Project docs

- Product brief: [PROJECT_BRIEF.md](./PROJECT_BRIEF.md)
- Upstream framework docs: [README.md](./README.md)
- Docker dev notes: [dev/README.md](./dev/README.md)

## 5. Recommended first implementation slice

Before we touch a lot of framework code, choose one narrow feature to build end-to-end. A good default is:

`custom communication workflow + light admin branding`

That gives us something visible quickly while keeping the upstream base stable.
