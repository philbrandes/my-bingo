# 🎉 Soc Ops — Social Bingo

> Break the ice, start conversations, and connect with people around you — one bingo square at a time.

**Soc Ops** is a fast, fun social bingo game built for in-person mixers, team events, and icebreakers. Find people who match the prompts on your card, tap to mark them off, and race to get **5 in a row**!

```
┌──────────┬──────────┬──────────┬──────────┬──────────┐
│  bikes   │  lived   │  has a   │ prefers  │  plays   │
│ to work  │ abroad   │   pet    │   tea    │instrument│
├──────────┼──────────┼──────────┼──────────┼──────────┤
│   runs   │ speaks   │  has     │   can    │  been    │
│marathons │2+ langs  │a garden  │  juggle  │skydiving │
├──────────┼──────────┼──────────┼──────────┼──────────┤
│   met    │  loves   │  FREE    │ left-    │  plays   │
│celebrity │ cooking  │  SPACE   │ handed   │vid games │
├──────────┼──────────┼──────────┼──────────┼──────────┤
│  does    │ hidden   │  loves   │ been     │collects  │
│  yoga    │ talent   │spicy food│  on TV   │something │
├──────────┼──────────┼──────────┼──────────┼──────────┤
│   read   │  knows   │  has a   │ born in  │  has a   │
│ a book   │   ASL    │   twin   │diff state│ traveled │
└──────────┴──────────┴──────────┴──────────┴──────────┘
```

## ✨ Features

- 📱 **Mobile-first** — designed for phones so everyone can play on their own device
- 🔀 **Randomized board** — every player gets a unique card shuffle
- 🎊 **Bingo celebration** — animated win state when you get 5 in a row
- ⚡ **Zero sign-up** — open the link, tap Start, play instantly
- 🚀 **Deploys to GitHub Pages** — share a link with your group in seconds
- 🎨 **Fully customizable** — swap in your own questions for any theme or event

## 🕹️ How to Play

1. **Share the link** with everyone at your event
2. Each person taps **Start Game** to get their shuffled card
3. **Mingle!** Find people who match the prompts — ask, discover, connect
4. **Tap a square** when you find someone who matches
5. First to get **5 in a row** (horizontally, vertically, or diagonally) wins 🏆

## 🚀 Quick Start

**Prerequisites:** [Node.js 22+](https://nodejs.org/)

```bash
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) to play locally.

## 🛠️ Build & Deploy

```bash
npm run build
```

Pushes to `main` automatically deploy to **GitHub Pages**.

## 🎨 Customize

Edit `src/data/questions.ts` to swap in your own prompts. The game always picks 24 random questions + the FREE SPACE, so add as many as you like:

```ts
export const questions: string[] = [
  "has a standing desk",
  "uses dark mode everywhere",
  "learned to code before 18",
  // ... add your own!
];
```

Theme ideas: team trivia, travel facts, tech skills, pop culture, office humor, and more.

---

Built with [React](https://react.dev/), [TypeScript](https://www.typescriptlang.org/), [Vite](https://vitejs.dev/), and [Tailwind CSS v4](https://tailwindcss.com/).
