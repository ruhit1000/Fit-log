# Fit-Log Development Tasks

- [x] **Task 1:** Initialize Next.js project, setup Tailwind CSS, install dependencies (Hero UI, Lucide React, react-hot-toast), and configure global CSS variables (colors/fonts).
- [x] **Task 2:** Create the global `WorkoutContext` (React Context) to manage local storage state for "Today's Plan" and "Saved Items" (including the 5-workout cap logic).
- [x] **Task 3:** Build the responsive `Navbar` component with dynamic badge counters synced to the Context, and create the static `Footer` component.
- [x] **Task 4:** Build the `HeroBanner` component using the provided banner image and logo assets, including the scroll-to-library CTA.
- [x] **Task 5:** Implement the API data fetching utility and build the reusable `WorkoutCard` component for the Library.
- [x] **Task 6:** Assemble the Home Page (`/app/page.tsx`) to display the Hero Banner and the responsive Workout Library grid, including the `loading.tsx` state.
- [x] **Task 7:** Build the Workout Details Page (`/app/workout/[id]/page.tsx`) layout (image on left, specs/instructions on right) and implement the 404 page (`not-found.tsx`).
- [ ] **Task 8:** Implement interactive CTA buttons on the Details Page ("Add to today's plan", "Save for later") with Context dispatch and toast notifications.
- [ ] **Task 9:** Build the My Plan Page (`/app/my-plan/page.tsx`) layout: Metrics Summary Row (dynamic calculation) and Hero UI Tabs structure.
- [ ] **Task 10:** Implement the `PlanItemCard` component and render the lists for "Today's Plan" and "Saved", handling Empty States correctly.
- [ ] **Task 11:** Add Challenge features to My Plan Page: "Mark as Done" functionality, "Remove (X)" functionality, and the Sort Dropdown (by Duration, Calories, Rating).
- [ ] **Task 12:** Final review, responsive design testing on all screens, verifying local storage persistence, and updating the project `README.md`.
