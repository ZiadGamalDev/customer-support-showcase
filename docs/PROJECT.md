# Customer Support System - Project Overview

A micro-services ecosystem of seven interconnected applications. Developed as an ITI Graduation Project in 2025 by a 5-person team, it simulates a setup where an e-commerce storefront embeds a live support widget that connects customers to support agents in real time.

## System Architecture

Two backend APIs and five specialized frontends.

### Core Components

1. **Customer Support API (Node.js/Express)**:
   - The central engine handling authentication, ticket routing, and real-time communication.
   - Agent assignment: picks the first AVAILABLE agent (unsorted), falling back to the first BUSY agent only if none are free under max load.
2. **E-commerce API (Node.js/Express)**:
   - Product management, user accounts, and order processing — demo data, not a live store.
3. **Agent Dashboard (React)**:
   - Agents manage active chats, update ticket statuses, and toggle availability.
4. **Admin Dashboard (Angular)**:
   - Manage users, monitor agent activity, and review chat history.
5. **E-commerce Storefront (React)**:
   - Product browsing and shopping cart.
6. **Customer Chat Widget (Angular)**:
   - Embedded widget for the storefront, real-time communication with support.
7. **E-commerce Admin Panel (React)**:
   - Product, category, and order management for the demo store.

## Technical Notes (verified against the code, 2026-10-13)

- **Real-time communication**: Socket.IO, 12 distinct event types. No latency benchmark exists in either repo, so no number is claimed.
- **Agent assignment**: not a sorted/"least busy" algorithm — see Core Components above.
- **State management**: agent status (Online, Busy, Away) and ticket status (New, Open, Pending, Resolved).
- **Authentication**: JWT-based, with email verification and role checks on both backends (support: admin/agent/customer; e-commerce: admin/user).
- **Deployment**: single PM2 fork instance per app behind Nginx — no horizontal scaling.
