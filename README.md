# Candidate Management – Next.js Mini App

A small Candidate Management application built with Next.js (App Router) that demonstrates basic CRUD-style functionality, local state management, and a clean UI.

## Features

- List candidates with **name, email, and role**.
- Add a new candidate using a validated form (required fields + basic email format).
- Delete an existing candidate from the list.
- Persist candidates using **localStorage**, so data remains after page refresh.
- Clean folder structure with **reusable components** for the form and list.

## Tech Stack

- Next.js (App Router, TypeScript)
- React Hooks: `useState`, `useEffect`
- Styling with Tailwind-style utility classes (can be plain CSS if preferred)
- Browser `localStorage` for simple persistence

## Getting Started

1. Clone the repository

```bash
git clone https://github.com/<ajay16ak>/candidate-management.git
cd candidate-management



2. Install dependencies
    npm install


3. Run the development server
    npm run dev


4. Open your browser at:
     http://localhost:3000


5. Project Structure
    app/
        page.tsx           # Main page: holds candidates state, localStorage sync, and layout

    components/
        CandidateForm.tsx  # Form to add a candidate with validation and error messages
        CandidateList.tsx  # Table to display candidates and handle delete actions


6. Implementation Details

 Candidates are stored in a candidates state array in app/page.tsx.
 On first render, the app loads any existing candidates from localStorage (key: candidates).
 Whenever the candidates array changes, it is serialized back into localStorage.
 Each candidate gets a unique id generated on the client.
 The form performs simple validation before submitting:
 Name, email, and role are required.
 Email must match a basic email pattern.


 7. ## How Requirements Are Met

    **Next.js with App Router**  
    Implemented using `create-next-app` with the App Router and `app/page.tsx` as the main page.

    **List candidates (Name, Email, Role)**  
    'CandidateList ' displays candidates in a table with columns for name, email, and role.

    **Form to add a new candidate**  
    'CandidateForm` collects name, email, and role and calls `onAdd` to update the candidates state.

    **Ability to delete a candidate**  
    Each row in `CandidateList` has a Delete button that triggers `onDelete` and removes that candidate from state.

    **Data stored in local state / localStorage**  
    `app/page.tsx` uses React state for candidates and synchronizes it with `window.localStorage` so data persists across refreshes.

    **Basic styling**  
    Tailwind-style utility classes provide a simple, clean layout, table, and buttons.

    **Clean folder structure**  
    The app code lives in `app/page.tsx` and two reusable components under `components/`.

    **Proper form validation**  
    `CandidateForm` enforces required fields and a basic email pattern, showing inline error messages when validation fails.
