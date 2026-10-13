# Customer Support System — Key Features

Verified against the code, 2026-10-13. Replaces the earlier `key-features.pdf`, which had
unsourced claims (see below) and was dropped — no PDF tooling available to regenerate it as a
PDF, so this is the corrected version.

## 1. Agent Assignment

- Automated ticket routing: new chats go to the first AVAILABLE agent (unsorted). If none are
  free, falls back to the first BUSY agent under max load.
- Dynamic reassignment: if an agent goes "Away" or disconnects, their active chats return to
  "Pending" and re-queue for the next available agent.
- Not a least-busy / workload-sorted algorithm — the original PDF claimed this; the code doesn't
  do it.

## 2. Real-Time Communication

- Built on Socket.IO: 12 distinct event types (4 client-to-server, 8 server-to-client) across
  per-chat and per-user rooms.
- Presence tracking: agent availability (Online, Busy, Away).
- No latency benchmark exists in either backend's repo — the original PDF's "Sub-50ms" figure
  had no source and isn't repeated here.

## 3. Logging

- Message histories persisted per chat.
- Ticket and agent-status transitions tracked.
- No dedicated analytics dashboard beyond the above — the e-commerce admin panel's overview
  numbers are hardcoded sample data, not a live query.

## 4. Architecture

- 7 applications: 2 Node.js/Express backends, 5 frontends (3 React, 2 Angular), each its own git
  repo.
- Each backend runs as a single PM2 fork instance — no horizontal scaling configured.
- Embeddable chat widget (Angular) can be dropped into any storefront via script tag or iframe.

## 5. Security

- JWT-based auth for API and WebSocket connections, on both backends.
- Role-based access: support API (admin/agent/customer), e-commerce API (admin/user).
- Email verification required before login, on both backends.
