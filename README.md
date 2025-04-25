
🔨 This project is currently under construction.

# 🟡 Yellot-arch

A pragmatic front-end architecture built for React Native + Expo projects.

Designed for **fast iteration**, **clean code**, and **real-world flexibility**.  
Inspired by the best of **Feature-based structure** and **React Native Clean Architecture**.

---

## 📁 Folder Structure

```txt
src/
│
├── app/                    # App routing and entry screens (Expo Router)
│
├── features/               # Feature-based *modules*
│   └── home/
│       ├── services/       # Logic, effects and services related to this module
│       ├── view/           # UI components (e.g. cards, modals)
│       ├── types.ts        # Types specific to the feature
│       └── index.tsx       # Screen-level composition for this feature
│
├── store/                  # Zustand store(s)
│
├── gateways/               # Integrations with APIs and libraries (e.g. analytics, firebase)
│   ├── firebase/               
│   └── backend/
│       ├── index.tsx       # General configurations of the integration (urls, pemissions, request/response structure, etc.)
│       └── modules/   
│           ├── types.ts    # Types specific to the backend module
│           └── api.tsx     # API entry for this backend module
│
├── shared/                 # Reusable pieces across the app
│   ├── components/         # Reusable UI components (Button, Input, etc.)
│   ├── types/              # Shared types (e.g. User, Session)
│   ├── utils/              # Utility functions (e.g. formatDate)
│   ├── hooks/              # Shared hooks
│   └── constants/          # Shared constants (colors, strings, etc.)
│
└── assets/                 # Fonts, images, etc. 
```

---

## 🔋 Stack

- **Expo SDK 51 or higher**
- **Tailwind css**
- **Zustand** for global state
- **TypeScript** first
- Clean & scalable by default

---

## 🧠 Philosophy

- Organize by **feature**, not by type
- Keep logic **outside the component**
- **Reusability** starts with separation
- Minimal but structured

---

## 🚀 How to Use

### Use as Template
```bash
npx create-expo-app MyApp --template blank
cd MyApp
git clone https://github.com/yellotmob/yellot-arch temp
mv temp/src temp/app temp/assets temp/.eslintrc.js temp/prettier.config.js .
rm -rf temp
npm install
npx expo start
```

---

## 🧩 Inspired by

- [React Native Clean Architecture](https://proandroiddev.com/clean-architecture-with-react-native-64f1fbc5a99d)
- [Feature-Sliced Design](https://feature-sliced.design/)
- [Vercel DX](https://vercel.com)
