# Customer Support System - Project Overview

The Customer Support System is a sophisticated micro-services ecosystem comprising seven interconnected applications. Developed as an ITI Graduation Project in 2025, it simulates a real-world infrastructure where e-commerce platforms integrate a live support widget that connects customers with dedicated support agents in real-time.

## System Architecture

The ecosystem is built on a modular architecture to ensure scalability and separation of concerns. It features two core APIs and five specialized frontends.

### Core Components

1.  **Customer Support API (Node.js/Express)**: 
    - The central engine handling authentication, ticket routing, and real-time communication.
    - Implements intelligent agent assignment logic based on availability and load.
2.  **E-commerce API (Node.js/Express)**:
    - Simulates product management, user activity logging, and order processing.
3.  **Agent Dashboard (React)**:
    - Specialized tool for support agents to manage active chats, update ticket statuses, and toggle availability.
4.  **Admin Dashboard (Angular)**:
    - High-level oversight for managing users, monitoring agent performance, and reviewing chat history.
5.  **E-commerce Storefront (React)**:
    - Consumer-facing application with integrated product browsing and shopping cart features.
6.  **Customer Chat Widget (Angular)**:
    - An embedded widget for the storefront that enables real-time communication with the support team.
7.  **E-commerce Admin Panel (React)**:
    - Management interface for products, categories, and orders within the e-commerce simulation.

## Technical Highlights

- **Real-time Communication**: Powered by Socket.IO with latency-optimized broadcasting.
- **Intelligent Routing**: Dynamic load balancing ensures tickets are assigned to the "least busy" available agent.
- **State Management**: Robust tracking of Agent Status (Online, Busy, Away) and Ticket Status (New, Open, Pending, Resolved).
- **Authentication**: Secure JWT-based auth with email verification and role-based access control (RBAC).

## Scalability and Performance

The system is designed to handle high-traffic environments through asynchronous processing and non-blocking I/O provided by the Node.js runtime. MongoDB provides a flexible schema for logging extensive activity and chat history, enabling detailed future analytics.
