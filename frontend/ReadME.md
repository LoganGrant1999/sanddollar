Frontend – React + TypeScript
React + TypeScript frontend for the Personal Finance AI app. Built with Vite and styled using TailwindCSS.

Run
To run the frontend service, use the following commands:

npm install
npm run dev

The frontend will be available at http://localhost:5173.

Features (initial)
Onboarding page that shows 3 example transactions

Dropdowns to assign categories (FOOD, RENT, INCOME, OTHER)

Submit button that mocks a backend call (or calls /api/categorize if backend is running)

Basic unit test verifying rendering and category changes

Scripts
Here are the available scripts for managing the frontend project:

npm run dev     # start dev server
npm run build   # production build
npm run preview # preview build locally
npm test        # run Vitest unit tests

Structure
The project structure is organized as follows:

src/
  main.tsx              # entry point
  App.tsx               # root component / router
  pages/Onboarding.tsx  # onboarding flow
  components/           # reusable UI components
  lib/api.ts            # fetch helpers (mock or real backend calls)
  styles/index.css      # Tailwind styles

Tests
To run the unit tests, use the following command:

npm test
