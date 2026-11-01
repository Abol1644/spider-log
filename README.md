# Spider Log

**Your Training. Your Progress. Your Data.**

Spider Log is a personal fitness and workout tracking application designed to help users plan training sessions, track performance, monitor body metrics, and understand their long-term progress.

The goal is to build a fast, focused, and visually distinctive fitness application with an emphasis on usability, structured workout tracking, and meaningful performance insights.

---

## Project Status

<escape>🚧</escape> **Early Development**

The initial Expo project has been created and tested. The UI design process has been completed in Google Stitch, and the exported design references are being prepared for native implementation.

Features and technical capabilities described in this document represent the intended product direction unless explicitly marked as implemented.

## Product Vision

Spider Log aims to provide a structured training experience without the unnecessary complexity commonly found in fitness applications.

The application should make it easy to:

- Create and manage workout programs.
- Track exercises, sets, repetitions, and weights.
- Record workout sessions efficiently.
- Monitor strength and body composition progress.
- Review training history and performance trends.
- Manage personal fitness information.

The product prioritizes clarity, speed, consistency, and user control over training data.

## Core Features

### 1. User Account & Onboarding

- Account registration and authentication.
- Multi-step profile setup.
- Personal information and body metrics.
- Fitness goals and training experience.
- Editable user profile.

### 2. Dashboard

- Overview of training activity.
- Current workout program.
- Recent workout sessions.
- Key performance metrics.
- Quick access to starting a workout.

### 3. Workout Programs

- Create and manage training programs.
- Organize exercises by training day.
- Configure sets, repetitions, and target weights.
- Import and export program configurations.

### 4. Active Workout

- Track an ongoing workout session.
- Record weight and repetitions for each set.
- Exercise demonstration media (GIF or video).
- Rest timer.
- Set completion tracking.
- Workout duration and session summary.

### 5. Training History

- Browse previous workout sessions.
- Review exercise performance.
- Inspect historical training records.
- Compare performance across sessions.

### 6. Analytics

- Strength progression.
- Training volume trends.
- Workout frequency.
- Body weight tracking.
- Progress visualization.

### 7. Profile & Settings

- Personal information management.
- Body metrics.
- Fitness goals.
- Measurement preferences.
- Application settings.

---

## Design System

The visual identity is based on a monochromatic AMOLED aesthetic with a distinctive green accent.

**Primary design principles:**

- Minimal and functional interfaces.
- High contrast and clear visual hierarchy.
- Sharp geometry and restrained corner radii.
- Large, readable numerical values.
- Minimal decorative elements.
- Fast and intuitive interactions.
- Consistent components across all screens.

**Primary color:**

`#03C39A`

The Google Stitch exports are the primary visual reference for implementation.

Refer to `design-reference/design.md` for the complete design system and visual specifications.

## Technology Direction

The application is being developed as a native-feeling cross-platform mobile application.

| Area                 | Technology                        |
| -------------------- | --------------------------------- |
| Mobile framework     | React Native                      |
| Development platform | Expo                              |
| Language             | TypeScript                        |
| Navigation           | Expo Router (proposed)            |
| UI direction         | Material 3-inspired custom design |
| Local persistence    | SQLite (proposed)                 |
| State management     | Zustand (proposed)                |

The final dependency selection and architecture must be verified against the existing project before implementation.

Avoid introducing unnecessary dependencies or replacing working infrastructure without a clear technical reason.

## Project Structure

The intended structure may evolve during implementation.

```text
spider-log/
├── design-reference/
│   ├── design.md
│   ├── screens/
│   │   ├── dashboard.html
│   │   ├── active-workout.html
│   │   └── ...
│   └── assets/
│       ├── logo.webp
│       └── logo.png
│
├── app/
├── assets/
├── components/
├── features/
├── hooks/
├── services/
├── stores/
├── types/
├── utils/
│
├── app.json
├── package.json
└── README.md
```

This is a proposed organizational structure, not a requirement to restructure the existing project immediately.

## Data Architecture Principles

The application should maintain a clear separation between user information, workout configuration, and workout history.

### User Account

Authentication-related information and account identity.

### User Profile

Personal information, body metrics, fitness goals, and training preferences.

### Exercise Library

Reusable exercise definitions, including:

- Exercise name and identifier.
- Target muscle groups.
- Equipment requirements.
- Instructions.
- Demonstration media URL.

### Workout Programs

Configurable training plans containing workout days and exercise prescriptions.

### Workout Sessions

Independent records of actual completed workouts, including:

- Session date and duration.
- Exercises performed.
- Sets, repetitions, and weights.
- Completion status.
- Session notes.

**Important:** Workout history must remain independent of workout program configuration. Editing or replacing a program must never silently modify previously recorded sessions.

## Development Principles

1. **Design fidelity:** Implement the provided designs as accurately as reasonably possible.
2. **Maintainability:** Prefer clear, modular, reusable code.
3. **Type safety:** Use TypeScript consistently.
4. **Offline-first direction:** Core workout tracking should eventually work without an internet connection.
5. **Data integrity:** Never silently discard workout history.
6. **Performance:** Keep screen transitions and workout interactions responsive.
7. **Accessibility:** Provide readable contrast, clear labels, and usable touch targets.
8. **Incremental delivery:** Implement and verify features in manageable phases.
9. **No unnecessary abstraction:** Keep the architecture appropriate for the actual product requirements.

## Design References

All exported Google Stitch references should be kept inside:

`design-reference/`

These files are implementation references and must not be modified during normal development.

- `design.md`: Design system and visual guidelines.
- `screens/`: Individual HTML screen exports.
- `assets/`: Logo and visual resources.

HTML files are reference materials. The production application must use native React Native components rather than rendering these pages through a WebView.

## Getting Started

### Prerequisites

- Node.js (compatible with the installed Expo SDK).
- npm, pnpm, or the package manager configured by the project.
- Expo-compatible Android or iOS development environment.

### Installation

```bash
npm install
```

### Start Development Server

```bash
npx expo start
```

Use the Expo terminal instructions to launch the application on an emulator, simulator, or supported physical device.

Refer to the official documentation for environment-specific setup:

- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/docs/getting-started)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)

## Roadmap

The planned development phases are:

- [ ] Project architecture and technical audit.
- [ ] Design tokens and shared UI components.
- [ ] Application navigation.
- [ ] Sign-up and onboarding.
- [ ] Dashboard.
- [ ] Workout program management.
- [ ] Active workout experience.
- [ ] Exercise library and demonstration media.
- [ ] Workout history.
- [ ] Analytics and progress tracking.
- [ ] Profile and settings.
- [ ] Local persistence and data management.
- [ ] Import and export functionality.
- [ ] Testing, optimization, and release preparation.

## Product Philosophy

Spider Log is not intended to be another fitness application filled with unnecessary features.

It should be a reliable training companion: simple enough to use during a workout, powerful enough to track long-term progress, and structured enough to preserve the user's training history.

**Train consistently. Track everything. Understand your progress.**
