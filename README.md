# FitLog 🏋️‍♂️

FitLog is a premium, no-nonsense workout library and planning application designed to help you train with intent. It allows users to browse a dynamic catalog of exercises, view detailed instructions, and seamlessly compile their daily workout plans.

## Features ✨

- **Workout Library:** A responsive, grid-based catalog of curated exercises fetched from a custom API.
- **Detailed Specifications:** Each workout has a dedicated details page featuring interactive Call-To-Action (CTA) buttons, difficulty ratings, muscle group tags, and step-by-step form instructions.
- **My Plan & Saved Workouts:** Add up to 5 workouts to your daily plan, or save them for later.
- **Challenge Mode (Metrics):** The "My Plan" page dynamically calculates your total estimated calories burned, workout duration, and exercise count in real time.
- **Workout State Management:** Workouts can be sorted by duration/calories/rating, marked as "Done" with visual strikethrough feedback, or removed entirely.
- **Persistent Storage:** All plans and saved workouts are synced instantly to the browser's `localStorage` via a custom React Context provider.

## Tech Stack 🛠️

- **Framework:** Next.js 16 (App Router)
- **Styling:** Tailwind CSS v4
- **UI Components:** HeroUI v3 (React Aria Components)
- **Icons:** Lucide React
- **Notifications:** React Hot Toast
- **Fonts:** Next/Font (Oswald for display, Inter for body)

## Getting Started 🚀

First, install dependencies:
```bash
npm install
```

Then, run the development server:
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the application in action.
