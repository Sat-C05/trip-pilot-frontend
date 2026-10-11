# TripPilot frontend

Coursework frontend submission: React 19, TypeScript and Vite. Source exported from the canonical [TripPilot project](https://github.com/Sat-C05/trip-pilot-java). The separate backend is [trip-pilot-backend](https://github.com/Sat-C05/trip-pilot-backend).

## Run and build

Use Node 22.12+ (22.x) or Node 24.x. Run `npm ci`, then `npm run dev`. Run `npm run build` for the TypeScript check and production assets in `dist/`.

The development proxy uses backend port 8002. For the existing local backend on 8082, set `$env:BACKEND_URL='http://127.0.0.1:8082'` in PowerShell before `npm run dev`. Configure and start the backend separately; this frontend contains no database or model credentials.

## Hosted application

The coursework demo is https://trip-pilot-java.vercel.app/ with backend https://trippilot-coursework.onrender.com. Included `vercel.json` proxies relative `/api` requests to that backend, including session authentication, CSRF and EventSource. If deploying this standalone repository, select the repository root, Vite, `npm ci`, `npm run build` and output `dist`. The existing deployment remains connected to the canonical repository.

## Coursework features and limits

Authentication, saved plans, card creation through research, persisted titles/personal notes, Trash/delete/restore, plan rename, comparison, selected-trip follow-ups, citations, Inspector and responsive layout. Evidence and model snapshots remain immutable. Public guide research can support destination information; current prices, availability and provider policies remain unavailable. Booking is disabled in the hosted demo; no real payment or reservation integration exists.

See the canonical project's [technical document](https://github.com/Sat-C05/trip-pilot-java/blob/main/project-document.md), [card management](https://github.com/Sat-C05/trip-pilot-java/blob/main/docs/card-management.md) and [deployment guide](https://github.com/Sat-C05/trip-pilot-java/blob/main/docs/coursework-deployment.md) for contracts and acceptance status. This source export does not establish new hosted acceptance or include personal records, credentials or internal notes.