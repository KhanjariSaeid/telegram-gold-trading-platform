# Multi-Bot Gold Trading Management System

A high-performance, asynchronous Telegram-based ecosystem designed to manage real-time gold trading rooms (Melting Gold/Talaye Ab-shodeh). This system orchestrates 5 specialized bots to handle high-traffic trading groups with over 2,000 active members.

## 🚀 System Architecture & Scalability

To ensure zero downtime and efficient load balancing, the system utilizes a **Distributed Multi-Bot Architecture**. Instead of a single bottleneck bot, the workload is distributed across 5 concurrent instances:

1.  **Registration & Wallet Bot:** Handles user onboarding, KYC data, asset status, and support tickets.
2.  **Core Trade Manager:** The brain of the system; matches buy/sell orders (Lafz) and executes trades.
3.  **Pricing Bot (Mazanneh):** Fetches real-time gold prices from global channels and broadcasts them (Manual/Automatic modes).
4.  **Reporting Bot:** Generates instant invoices (PDF) and daily trade summaries.
5.  **Cleaner/Moderator Bot:** Maintains group hygiene by removing redundant messages and formatting user inputs.

## 🛠 Tech Stack

*   **Language:** Python 3.10+
*   **Library:** `python-telegram-bot` (Advanced use of `Application`, `Context`, and `Ext` modules)
*   **Concurrency:** Fully Asynchronous (`asyncio`) to handle thousands of concurrent requests without blocking.
*   **Database:** SQLite3 with optimized relational schemas for transactional integrity.
*   **Document Generation:** Automated PDF generation for official trade invoices.

## ✨ Key Features

*   **Asynchronous Processing:** Built from the ground up using `async/await` patterns, ensuring the system remains responsive under heavy load from 2,000+ users.
*   **Auto-Price Synchronization:** Features an automated pricing engine that tracks market fluctuations and updates the trading group at configurable intervals.
*   **Trade Matching Engine:** Automatically detects matching buy/sell prices among users, "locks" the trade, and issues digital invoices.
*   **High Availability & Health Monitoring:** Implemented a "Heartbeat" mechanism where bots monitor each other's status. If one bot goes offline, the others immediately notify the administrator.
*   **Security & Logs:** Comprehensive logging system for real-time debugging and error tracking via terminal outputs.

## 📈 Performance & Impact

*   **User Base:** Active management of a 2,000-member professional trading community.
*   **Production Ready:** The system is currently deployed in three distinct versions:
    *   *1-Gram Trading Version*
    *   *10-Gram Trading Version*
    *   *Demo/Simulator Version* (for educational purposes and training new traders).
*   **Efficiency:** Development evolved through iterative cycles (approx. 2 months per major module), resulting in a modular codebase that allows for rapid deployment of new instances.

## 🛡 Disclaimer
The source code for this project is proprietary and owned by the client. This repository serves as a portfolio to showcase the architectural design, logic implementation, and technical challenges overcome during development.

---
*Developed with obsession for detail and performance.*
