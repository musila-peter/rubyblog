---
title: "CoolHarlems Inventory System — Offline-First PWA"
date: 2026-03-30 11:35:00 +0300
categories: [Work, Case Study]
tags: [React, FastAPI, PostgreSQL, Supabase, PWA]
---

## Overview
Engineered a comprehensive, full-stack Inventory Management System featuring deep POS (Point of Sale) integration and offline-first Progressive Web App (PWA) capabilities for a medium-sized retail business.

## The Objective
To create a dependable stock tracking and sales analytics platform that continues to function flawlessly even during internet outages, a vital requirement in low-connectivity retail environments. The system enables real-time automated inventory reconciliation across any device while keeping critical retail operations running offline.

## System Architecture & Stack
- **React & PWA**: A snappy, device-agnostic frontend leveraging IndexedDB to cache interactions locally when offline.
- **FastAPI**: Handles backend orchestration, inventory math, and securely processes batched online synchronizations.
- **PostgreSQL**: Serves as the central source of truth for stock quantities, reporting, and large-scale sales analytics.
- **Supabase**: Real-time capabilities for dashboarding and rapid cross-device synchronization once connections are restored.

## The Technical Challenges
- **Data Synchronization**: Complex bidirectional synchronization was required between the local IndexedDB stores and the central REST API.
- **Transaction Integrity**: The hardest aspect was ensuring 100% data integrity during offline-to-online transitions to prevent stock desyncs (e.g. double-counting offline sales the moment connectivity returned).

## Metrics & Impact
- **100% Offline Uptime**: Achieved perfect reliability for critical checkout and sales logging tasks.
- **Sub-500ms Response Times**: Fast localized operations via IndexedDB boosted checkout efficiency immensely.
- **Server Load**: Greatly reduced sustained backend load by safely batching requests locally.

## Links
- **Live Platform**: [me-inventory.vercel.app](https://me-inventory.vercel.app/)
- **Source Code**: [GitHub Repository](https://github.com/peter-kiilu)
