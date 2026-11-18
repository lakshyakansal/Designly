# Designly — Canva-inspired Design Platform

A full-stack starter for a professional graphic-design SaaS with a React web app, React Native mobile app, and Java Spring Boot API.

## Architecture
- `web/`: React + Vite web application with a responsive dashboard and lightweight design editor.
- `mobile/`: Expo React Native application starter.
- `backend/`: Spring Boot REST API with project CRUD endpoints and PostgreSQL configuration.

## Run locally

### Backend
Requires Java 17+ and Maven.
```bash
cd backend
mvn spring-boot:run
```
API: `http://localhost:8080/api/projects`

### Web
Requires Node.js 20+.
```bash
cd web
npm install
npm run dev
```
Open `http://localhost:5173`.

### Mobile
Requires Node.js and Expo.
```bash
cd mobile
npm install
npx expo start
```

## Current MVP scope
- Responsive dashboard and design workspace
- Starter templates and project cards
- Add text and basic shapes to a simple editor canvas
- Save projects through the backend API
- Mobile app navigation starter

## Before production
Add authentication (JWT/OAuth), role-based access, persistent design-document schema, object storage for uploads/exports, collaborative editing via WebSockets, payments, moderation, rate limiting, observability, backups, and automated tests. The editor is an MVP foundation, not a complete Canva-equivalent editor.

## Full editor MVP (added)
The web editor now uses Fabric.js and includes:
- Drag/move/select objects on a 1080×1080 canvas
- Text objects with inline editing, font family, size, bold, italic, alignment and color
- Rectangle and circle elements with fill and opacity controls
- Local image upload and canvas placement
- Template presets, layer selection, duplicate and delete
- Canvas background controls
- PNG export and PDF export

Run `npm install` again in `web/` after updating dependencies. Browser file uploads are local to the session; cloud persistence and multi-user collaboration still need backend integration.
