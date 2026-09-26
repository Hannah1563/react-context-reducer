# **React Guided Learning Activity: Theme Switcher & useReducer**

**Title:** Implementing a Theme Switcher with useContext & State Management with useReducer

**Objective:** Learn how to use the React Context API (`useContext`) for **global state management** (theme switching) and `useReducer` for **managing complex state** (task manager).

---

## **Tools:**
* GitHub Classroom
* GitHub Codespaces (or a local development environment with Node.js and a suitable IDE like VS Code)
* Vite
* React
* TypeScript

---

## **Color Palette**
Use these colors for styling:

```
Light Theme
===========
Background: #FFFFFF
Text: #000000
Button: #1E90FF

Dark Theme
===========
Background: #242629
Text: #FFFFFF
Button: #85D1B0
```

---

## **Getting Started**

```bash
npm install
npm run dev
```

The app runs at `http://localhost:5173/`.

---

## **Project Structure**

```
src/
├── constants/
│   └── theme.ts          # Light/dark theme constants
├── context/
│   └── ThemeContext.tsx   # Theme context, provider, and custom hook
├── reducers/
│   └── taskReducer.ts    # Typed reducer for task management
├── components/
│   ├── Navbar.tsx         # Navbar with theme toggle button
│   ├── Navbar.module.css
│   ├── TaskManager.tsx    # Task add/remove using useReducer
│   └── TaskManager.module.css
├── App.tsx                # Root component wrapped with ThemeProvider
└── main.tsx
```

---

## **Part 1: Theme Switcher with useContext**

- `constants/theme.ts` exports `LIGHT_THEME` and `DARK_THEME` string constants.
- `context/ThemeContext.tsx` creates a typed context, a `ThemeProvider` component, and a `useTheme` custom hook.
- `components/Navbar.tsx` consumes `useTheme` to display a button that toggles between light and dark mode.

## **Part 2: Task Manager with useReducer**

- `reducers/taskReducer.ts` defines typed `Task`, `State`, and `Action` types with `add` and `remove` cases.
- `components/TaskManager.tsx` uses `useReducer` with `taskReducer` to add and remove tasks, and applies theme styles via `useTheme`.
