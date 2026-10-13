# Customer Support System

A real-time Customer Support System integrated with a demo E-Commerce platform. Developed as an ITI Graduation Project in 2025 by a 5-person team, this ecosystem consists of 7 connected applications built with Node.js, MongoDB, Socket.IO, React, and Angular.

Personal/educational project, not client work. Parked since late 2025 — no commits across any of the 7 repos since.

## System Architecture

| Component           | Description                                            | Technologies                |
| -------------------- | -------------------------------------------------------- | ---------------------------- |
| **Support API**     | Core engine for auth, ticket routing, and real-time sockets. | Node.js, Express, Socket.IO |
| **E-commerce API**  | Demo store backend: products, orders, user accounts.   | Node.js, Express, MongoDB   |
| **Agent Dashboard** | Interface for agents to handle live tickets.            | React, Socket.IO            |
| **Admin Panel**     | Management for agents and chats.                        | Angular                     |
| **Storefront**      | Customer-facing e-commerce interface.                   | React, Tailwind CSS         |
| **Chat Widget**     | Embeddable real-time support widget.                     | Angular                     |
| **Shop Admin**      | Management of products and categories.                  | React                       |

## Technical Capabilities (verified against the code, 2026-10-13)

- **Real-time chat over Socket.IO**, 12 distinct event types across per-chat and per-user rooms.
- **Two independently-deployed backends share one login.** A customer's token, issued by the e-commerce API, is validated by the support API through a live cross-service check — so a shopper's chat session and their store account stay the same identity without a shared database.
- **Ticket state machine** (new, open, pending, resolved) with automatic reassignment: if an agent goes "Away" or disconnects, their open chats return to the queue for the next available agent.
- **Role-based access and email-verified signup** on both backends (support: admin/agent/customer; e-commerce: admin/user).
- **103 REST endpoints, 18 MongoDB collections**, across the two backends.

## Contributors

Built by a 5-person ITI team. [Ziad Gamal](https://github.com/ZiadGamalDev) was the primary author of the core support API (`customer-support-node`, ~87% of that repo's commits — auth, the Socket.IO layer, agent-assignment logic, cross-backend auth integration), and a contributing team member (15-48% commit share), not lead, on the other six repos.

## Documentation

- [System Architecture](docs/PROJECT.md)
- [Key Features](docs/key-features.md)
- `docs/Business-Model.pdf`, `docs/ITI-Graduation-Project-Discussion.pdf` — original ITI coursework deliverables (business-model pitch and graduation presentation). They describe aspirational/planned scope (subscription pricing, an AI chatbot, a 99.9% uptime SLA, Shopify/WhatsApp integrations) that was not built in this codebase — kept for context, not as a feature list.

## Live Demo

[customer-support-agent.ziadgamal.com](https://customer-support-agent.ziadgamal.com)

The apps are live and the login screens/shells load, but the project has been parked since late 2025 and currently has a backend connectivity issue (MongoDB Atlas unreachable from the VPS) — data views don't render. Treat this as a code sample, not a working live demo.

## License

MIT.

---
[Contact & Portfolio](https://ziadgamal.com)
