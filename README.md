# Customer Support System

A large-scale, real-time Customer Support System integrated with a sophisticated E-Commerce infrastructure. Developed as an ITI Graduation Project in 2025, this ecosystem consists of 7 fully connected applications built with Node.js, MongoDB, Socket.IO, React, Angular, and Express.

## System Architecture

The ecosystem comprises two primary backend services and five frontend applications, creating a complete end-to-end support environment.

| Component           | Description                                           | Technologies                |
| ------------------- | ----------------------------------------------------- | --------------------------- |
| **Support API**     | Core engine for auth, routing, and real-time sockets. | Node.js, Express, Socket.IO |
| **E-commerce API**  | Simulates customer data and activity logs.            | Node.js, Express, MongoDB   |
| **Agent Dashboard** | Interface for agents to handle live tickets.          | React, Socket.IO            |
| **Admin Panel**     | Over-arching management for agents and chats.         | Angular                     |
| **Storefront**      | Customer-facing e-commerce interface.                 | React, Tailwind CSS         |
| **Chat Widget**     | Real-time support interface for customers.            | Angular                     |
| **Shop Admin**      | Management of products and categories.                | React                       |

## Technical Capabilities

- **Real-Time Infrastructure**: Sub-100ms message delivery using a robust Socket.IO implementation.
- **Intelligent Routing**: Automated ticket assignment to the least busy agent, ensuring balanced workload distribution.
- **State Management**: Comprehensive tracking of agent availability (Online, Busy, Away) and ticket lifecycle (New, Open, Pending, Resolved).
- **Production-Ready Auth**: JWT-based authentication with email verification and role-based access controls.

## Business Impact

The system demonstrates a scalable solution for high-volume customer interaction. By automating ticket routing and providing real-time oversight, it significantly reduces response times and improves agent efficiency. The modular design allows for independent scaling of each component based on demand.

## Live Demonstrations

| Application          | Production Link                                                                      |
| -------------------- | ------------------------------------------------------------------------------------ |
| **Agent Dashboard**  | [customer-support-agent-react](https://customer-support-agent-react.vercel.app/)     |
| **Admin Dashboard**  | [customer-support-admin-angular](https://customer-support-admin-angular.vercel.app/) |
| **E-Commerce Store** | [ecommerce-react-two-pi.vercel.app](https://ecommerce-react-two-pi.vercel.app/)      |

## Documentation

Comprehensive technical documentation is available in the `docs/` directory:
- [System Architecture](docs/PROJECT.md)
- [Key Features Guide](docs/key-features.pdf)

## Contributors

Developed by a dedicated team of 5 developers. Main architectural and backend development by [Ziad Gamal](https://github.com/ZiadGamalDev).

## License

This project is licensed under the MIT License.

---
[Contact & Portfolio](https://ziadgamal.com)
