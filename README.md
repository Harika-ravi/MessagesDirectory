# 📱 Messages Directory

A polished React Native mobile app — an animated splash screen leading into a searchable directory of message categories, each opening a chat-style view where messages can be read, sent, and marked as read.

**Course:** CS5450 — Mobile Programming
**Instructor:** Dr. Sabah Mohammed
**Author:** Harika Ravi (Student ID: 1332239)
**Exercise: 3** — React Native Messages Directory

---

## ✨ Features

| Feature | Description |
|---------|-------------|
|  **Animated Splash** | Logo scales and fades in, then auto-navigates to the directories after ~2 seconds. |
|  **Directories Grid** | Six colorful category cards (You, Home, Love, Family, Friends, School) with gradient icons and live unread badges. |
|  **Search Bar** | Filter directories by name in real time. |
|  **Unread Filter** | Toggle to show only directories that contain unread messages. |
|  **Chat Screen** | Messages render as chat bubbles — sent messages align right, received align left with sender avatars. |
|  **Message Composer** | Type and send a new message; the list auto-scrolls to the newest message. |
|  **Mark All Read** | A header button clears unread indicators for the open directory; counts update everywhere instantly. |

---

## 🛠️ Technology Stack

- **React Native** — cross-platform mobile framework
- **Expo (SDK 54)** — tooling and runtime for building and running the app
- **Expo Router** — file-based navigation between screens
- **TypeScript** — typed JavaScript for safer, self-documenting code
- **React Context** — lightweight shared state store (no external state library)
- **expo-linear-gradient** & **@expo/vector-icons** — gradients and icons for the UI

---

## 📂 Project Structure

```text
MessagesDirectory/
├── app/                       # All screens (Expo Router)
│   ├── _layout.tsx            # Root layout: navigation stack + StoreProvider
│   ├── index.tsx              # Animated splash / welcome screen
│   ├── directories.tsx        # Main grid: search + unread filter
│   └── messages/
│       └── [id].tsx           # Chat screen: bubbles + composer + mark-as-read
├── data/
│   └── messages.tsx           # App data + shared store (React Context)
├── theme/
│   └── theme.ts               # Design system: colors, spacing, fonts, shadows
├── assets/                    # App icons & images
├── app.json                   # Expo configuration
├── package.json               # Dependencies & scripts
└── tsconfig.json              # TypeScript configuration
```

### Key files explained

- **`app/_layout.tsx`** — Defines the navigation stack and wraps the app in the shared data store (`StoreProvider`).
- **`app/index.tsx`** — The animated splash screen shown on launch; auto-navigates to the directories.
- **`app/directories.tsx`** — The main grid of categories with a search bar and an unread-only filter.
- **`app/messages/[id].tsx`** — The chat screen for a selected category, including the message composer and mark-as-read.
- **`data/messages.tsx`** — Holds all categories and messages and provides the shared store with `sendMessage` and `markAllRead`.
- **`theme/theme.ts`** — The central design system (colors, spacing, radii, font sizes, shadows) reused across all screens.

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) (LTS version) — verify with `node -v`
- **Android Studio** with an Android Virtual Device (emulator), **or** the **Expo Go** app on a physical phone

### Installation & Running

1. **Clone the repository**
```bash
   https://github.com/Harika-ravi/MessagesDirectory.git
   cd MessagesDirectory
```

2. **Install dependencies**
```bash
   npm install
```

3. **Start the development server**
```bash
   npx expo start -c
```

4. **Open the app**
   - Press **`a`** to launch on an Android emulator
   - Press **`w`** to run in a web browser (Chrome)
   - Or scan the QR code with the **Expo Go** app on a physical phone

> 💡 **Note:** The app does not use a database. All message data is stored in a simple in-memory list, as permitted by the exercise.

---

## 📖 How to Use

1. On launch, the **animated splash screen** appears for about two seconds.
2. The **Directories** screen lists all message categories with live unread badges.
3. Use the **search bar** to filter directories by name, or toggle **"Unread only"** to focus on directories with new messages.
4. **Tap any directory** to open its chat screen and read the stored messages.
5. Type in the **composer** at the bottom and press send to add a new message.
6. Tap the **checkmark** button in the top-right to mark all messages in that directory as read.

---

## 📸 Screenshots



> To add screenshots: create a `screenshots/` folder in the repo, upload your images, then replace the cells above like `![Splash](screenshots/splash.png)`.

---

## 📝 License

This project was created for educational purposes as part of CS5450 at Lakehead University.
