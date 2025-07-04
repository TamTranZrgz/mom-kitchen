# MOM KITCHEN

## Project Setup

- create project folder

```bash
mkdir mom-kichen
```

- inside project folder

```bash
git init # init git repo

pnpm init # create package.json fole

pnpm add -D turbo ## install turbo, will create pnpm-lock.yaml file automatically

```

- create `turbo.json` file - configuration file that tells Turborepo how to run tasks across monorepo

- create `pnpm-workspace.yaml` file - tells pnpm (and Turborepo) where your apps and shared packages live.

- create `apps` folder

- create `nextjs` app, inside `./apps/web`

```bash
pnpm create next-app .
```

- create `nestjs` app, inside `./apps/api`

```bash
pnpm create nestjs@latest api
```

- in `package.json` file of `api`, change `start:dev` to `dev` to make it consistent for monorepo.

- run project

```bash
pnpm run dev
```

## Integrate Prisma

- inside `apps/api`, install `prisma`

```bash
pnpm add -D prisma

pnpm add @prisma/client

npx prisma init --datasource-provider sqlite
```

- add entiies (User, Post, Recipe, Category, Tag, Like, Commmnent)

- migrate prisma schema and run prisma studio

```bash
npx prisma migrate dev --name init

npx prisma studio
```

## Reference

[Full-Stack Blog App with NestJS, NextJS & Turborepo – 10-Hour Ultimate Guide](https://www.youtube.com/watch?v=rsRglxTKbR0)
