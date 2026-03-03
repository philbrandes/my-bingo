# Soc Ops Copilot Instructions

## Mandatory Development Checklist

**ALWAYS run these before making changes:**
- [ ] 
pm run lint (0 errors/warnings required)
- [ ] 
pm run build (TypeScript + Vite build success)  
- [ ] 
pm run test (21/21 tests passing)

## Project Overview

**Soc Ops** is a social bingo game for in-person mixers. React 19 + TypeScript + Vite + Tailwind CSS v4. Players find others matching icebreaker questions to get 5-in-a-row bingo. Auto-deploys to GitHub Pages.

## Key Architecture

### Core Files
- **[src/App.tsx](src/App.tsx)** - Main app; game flow orchestration
- **[src/hooks/useBingoGame.ts](src/hooks/useBingoGame.ts)** - Game state + localStorage persistence  
- **[src/utils/bingoLogic.ts](src/utils/bingoLogic.ts)** - Pure game logic (heavily tested)
- **[src/data/questions.ts](src/data/questions.ts)** - 24 icebreaker questions array
- **[src/types/index.ts](src/types/index.ts)** - Domain types

### Components (src/components/)
- **StartScreen/GameScreen** - Main UI screens
- **BingoBoard/BingoSquare** - 5×5 grid + individual squares
- **BingoModal** - Win celebration

### Game Logic
- **Board:** 24 random questions + 1 center free space
- **Win Detection:** 8 lines (5 rows, 5 columns, 2 diagonals)
- **State:** 'start' | 'playing' | 'bingo' with localStorage persistence

## Commands

`ash
npm run dev      # Vite dev server (http://localhost:5173)
npm run build    # Production build  
npm run lint     # ESLint check
npm run test     # Vitest run
`

## Coding Standards

### TypeScript
- Strict mode enabled; no ny types
- Explicit interfaces for component props
- Type guards for localStorage validation

### React
- Functional components only
- useCallback for event handlers passed as props
- useMemo for expensive computations

### Tailwind CSS v4
- CSS-first config via @theme directive in [src/index.css](src/index.css)
- Mobile-first responsive design
- See [.github/instructions/tailwind-4.instructions.md](.github/instructions/tailwind-4.instructions.md)

## Critical Guidelines

1. **Preserve Game Logic** - [src/utils/bingoLogic.ts](src/utils/bingoLogic.ts) has 21 tests; changes require test updates
2. **Question Structure** - [src/data/questions.ts](src/data/questions.ts) must have exactly 24 items
3. **localStorage Validation** - Always validate StoredGameData (see useBingoGame pattern)
4. **No Mutations** - Use immutable updates; return new arrays/objects
5. **TypeScript Strict** - Fix types properly; avoid assertions (s)

## Custom Agents Available

- **Pixel Jam** - UI design iterations with visual feedback
- **Quiz Master** - Generate themed icebreaker questions  
- **TDD (Red/Green/Refactor)** - Test-driven development
- **UI Review** - UX/accessibility review

## Testing Strategy

- **Core Logic:** 21 tests in ingoLogic.test.ts
- **Test Environment:** Vitest + jsdom
- **Coverage:** Board generation, win detection, state mutations

## Design Guidelines

- **Inclusive Questions:** Safe for all; avoid sensitive topics
- **Balanced Difficulty:** 40-60% easy wins; mix personal/work/fun
- **Mobile-First:** Touch-friendly (44px+ squares)
- **Performance:** <200KB gzipped bundle

## Deployment

Auto-deploys to GitHub Pages on main push. Base path auto-detected from repo name.

---

**Version:** 1.0 | **Updated:** March 3, 2026
