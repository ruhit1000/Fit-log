# Fit-Log Architecture & Implementation Plan

## 1. Project Overview
A responsive Next.js web application for browsing, planning, and tracking workouts, utilizing local storage for state persistence. Designed with a dark, high-contrast aesthetic.

## 2. Tech Stack
- **Framework:** Next.js (App Router)
- **Styling:** Tailwind CSS
- **UI Components:** Hero UI, Lucide React (Icons)
- **State Management:** React Context API + `localStorage`
- **Notifications:** React Hot Toast (or Sonner)

## 3. Data Architecture
Data is fetched server-side from external API (`https://api.api-store.workers.dev/api/fitlog`). 
Local storage stores the user's active selections (arrays of workout objects or IDs) partitioned into two lists: `planItems` (Today's Plan) and `savedItems` (Saved for later).

## 4. Application Routing
### Server-Side Routes
- `/`: Home page - Fetches all workouts, displays Hero Banner and Workout Library Grid.
- `/workout/[id]`: Detail page - Fetches specific workout info by ID. Handles invalid routes via `not-found`.

### Client-Side Routes
- `/my-plan`: Plan tracking dashboard. Reads `localStorage` data to render active items. Includes dynamic summary metrics and custom sorting.

### Special Files
- `not-found.tsx`: Custom 404 fallback page.
- `loading.tsx`: Loading state skeleton for home page fetching.

## 5. State Management (Context API)
- `WorkoutProvider`: Wrapper context exposing state and dispatch functions.
- Enforces business logic: maximum 5 workouts allowed in "Today's Plan".
- Automatically serializes to/from `localStorage` on client mount to persist data across reloads.

## 6. Key Components
- **Navbar:** Sticky or static nav with Logo (from assets) and reactive badge counters hooked to the Context API.
- **Hero Banner:** Incorporates the provided banner asset with a call-to-action anchor link.
- **Library Grid:** Responsive grid mapping (`grid-cols-1 md:grid-cols-2 lg:grid-cols-3`).
- **Cards:** Abstracted into `WorkoutCard` (for the library) and `PlanItemCard` (for My Plan with specific action buttons).

## 7. Build & Deployment
Application needs to be strictly typed/checked to ensure 0 build errors. Designed for edge-ready deployment on Vercel or Cloudflare.
