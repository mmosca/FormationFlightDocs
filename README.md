# FormationFlight.org Docs

![License](https://img.shields.io/github/license/FormationFlight/Docs)
[![Chat](https://img.shields.io/discord/1120104184725905443)](https://discord.gg/npaX3VxQjh)

FormationFlight.org website source code

## Need help? Confused? Join the Community!

- [Discord Chat](https://discord.gg/npaX3VxQjh)

## Installation

You need to have [docker](https://docs.docker.com/engine/install/)
and [docker-compose](https://docs.docker.com/compose/install/) installed in your environment.

If you edit the docs in vscode when you open the top level directory it will ask if you wish to `Reopen in Container` click that button and vscode will automatically run `docker compose up` which will then start serving the documentation as below, otherwise you can do it manually as below.

Then you need to build your container:

```
docker compose build
```

and start mkdocs server:

```
docker compose up
```

After server is running visit [http://localhost:8000/](http://localhost:8000/).
