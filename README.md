# react-node-test-assessment

## Repository Layout
- `api/` – Express backend (messages, file uploads)
- `app/` – React frontend scaffold

## Prerequisites
- Node.js 22+
- pnpm (recommended) or npm

## Quick Start

```bash
# backend
cd api
cp env.example .env
pnpm install
pnpm dev                # starts on http://localhost:3001

# frontend
cd ../app
cp env.example .env
pnpm install
pnpm dev                # starts on http://localhost:3000
```

## Environment Variables

**api/.env**
PUSHER_APP_ID=your_app_id
PUSHER_KEY=your_key
PUSHER_SECRET=your_secret
PUSHER_CLUSTER=your_cluster

**app/.env**
REACT_APP_PUSHER_KEY=your_key
REACT_APP_PUSHER_CLUSTER=your_cluster

## Completed Challenges

### Challenge 1: Real-time messages with Pusher
- Pusher wired on the backend to publish new-message and message-deleted events
- Frontend subscribes to the chat channel and live updates the message list
- Messages append on new-message and are removed on message-deleted

### Challenge 2: Message search endpoint and realtime filter
- GET /api/messages/search?q=term added (case-insensitive, newest first, max 100 results)
- Search input with 300ms debounce added to the frontend
- Loading and empty states handled
- Live Pusher feed continues when search is cleared