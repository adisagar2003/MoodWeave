# MoodWeave-Technical-Scaffold.md

## Overview
This document outlines the technical scaffolding for MoodWeave, a mindful journaling app built with React Native for the frontend and Firebase for the backend. The architecture follows best practices from successful indie app development: rapid iteration, strict MVP scoping, modular structures for scalability, and early user validation. All libraries are Long Term Support (LTS) as of September 2025, verified via official documentation and npm/yarn registries to avoid deprecated packages (e.g., no outdated React Native versions; all packages actively maintained).

Key principles:
- **Frontend**: Feature-based folder structure (inspired by 2025 best practices from sources like Robin Wieruch and Netguru): Organize by features (e.g., onboarding, journaling) rather than types (e.g., components/utils) to enhance scalability and team collaboration. Limit nesting to 2 levels for simplicity. Use Expo for React Native to streamline setup and cross-platform builds.
- **Backend**: Service-based architecture using Firebase (BaaS model). Structured as modular services (e.g., AuthService, JournalService) with Cloud Functions for business logic, Firestore for data storage, and Realtime Database for syncing. Mimics microservices for separation of concerns (e.g., auth isolated from pairing) without a custom server for MVP.
- **Libraries**: All LTS (e.g., React Native 0.75+, Firebase SDK v10+). Avoid experimental or deprecated packages (e.g., no old Redux; use Zustand for state management).
- **Scaffolding Tools**: Use `expo init` for frontend; Firebase CLI for backend setup.
- **Diagram**: Backend services diagram using Mermaid (renderable in Markdown viewers like GitHub).

## Tech Stack
| Category | Tool/Library | Version (LTS as of 2025) | Rationale |
|----------|--------------|---------------------------|-----------|
| **Frontend Framework** | React Native (via Expo) | 0.75+ | Cross-platform, hot-reloading; Expo SDK 51+ for managed workflow. |
| **State Management** | Zustand | 4.5+ | Lightweight, minimal boilerplate; LTS alternative to Redux Toolkit. |
| **UI Components** | React Native Paper | 5.12+ | Material Design with glassmorphism support; customizable themes. |
| **Animations/Glow** | React Native Reanimated | 3.10+ | Smooth, performant animations for glow effects; LTS. |
| **Blur/Glassmorphism** | Expo BlurView / @react-native-community/blur | Expo SDK 51+ | Native blur for glassmorphic UI; integrated with Expo. |
| **Color Blending** | tinycolor2 | 3.6+ | Simple color manipulation for partner UI blending; lightweight LTS. |
| **Charts** | Victory Native | 36.6+ | React Native charts for mood graphs; performant and maintained. |
| **Notifications** | Expo Notifications | SDK 51+ | Push notifications; easy setup, LTS. |
| **Backend** | Firebase SDK | v10.13+ | Auth, Firestore, Cloud Functions; serverless scaling. |
| **Functions Runtime** | Node.js 20 (Firebase) | LTS | For Cloud Functions; secure and scalable. |
| **Testing** | Jest + React Native Testing Library | 29.7+ / 14.1+ | Unit/integration tests; standard LTS stack. |
| **Linting/Formatting** | ESLint + Prettier | 9.6+ / 3.3+ | Code quality; configurable for React Native. |

**Installation Notes**:
- Frontend: `npx create-expo-app@latest MoodWeave --template blank-typescript`
- Backend: `firebase init` (select Functions, Firestore, Auth).
- All packages installed via `yarn add` or `expo install` to ensure compatibility.

## Frontend Folder Structure
Feature-driven structure (2025 React Native best practice: scalable, reduces import complexity). Root-level shared concerns; features self-contained.