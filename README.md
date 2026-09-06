# DdaAdhd

> **Experimental TypeScript web application with books, lessons and marketplace views**

Despite the repository name, the tracked implementation is a full-stack
TypeScript web-app scaffold rather than a DDoS-defence service. The React
client contains views for books, lessons, a marketplace, registration and
administration; the server provides tRPC, authentication helpers, storage and
Drizzle database definitions.

## Structure

```text
client/src/pages/     Home, Books, Lessons, Marketplace, Admin and Register
server/               tRPC server, auth, database and storage
drizzle/              schema relations and initial migration
userGuide.md          existing user-oriented material
SECURITY.md            repository security guidance
```

## Requirements and local development

The repository declares pnpm 10.4.1 through its lockfile:

```bash
pnpm install
pnpm dev
```

Available validation commands are:

```bash
pnpm check
pnpm test
```

`pnpm db:push` generates and migrates the Drizzle schema. Use it only with a
development database after reviewing the target configuration.

## Configuration

The server includes environment and OAuth helper modules under `server/_core/`.
The required service values are not documented as a safe sample in this
repository. Configure them locally and keep database URLs, client secrets and
session material out of Git.

## Status

The application is experimental. Content-focused page names reflect available
screens, not a claim that the user flows, authentication, payments or data
storage are production-ready. The old README text about DDoS is not supported
by the current tracked application and has been replaced by this source-based
overview.

## Licence

No root licence file is present.
