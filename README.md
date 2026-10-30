# CHRONO-FLOW

A self-contained, responsive focus workspace. The complete application—HTML, CSS, SVG icons, and vanilla JavaScript—is in **index.html**. No build step, framework, package installation, or API key is required.

## Run

Open `index.html` in a modern browser, or serve this directory:

```sh
python -m http.server 8766 --bind 127.0.0.1
```

Then visit http://localhost:8766. For deployment, upload `index.html` to any static HTTPS host.

## Included

- Editable Pomodoro sessions, four-session cycles, auto-transition, daily focus history and streaks.
- Local digital and sweeping analog clocks, searchable IANA world timezones, date-aware offsets.
- Stopwatch with millisecond display, laps, split differences, fastest/slowest/average splits.
- Countdown presets and manual hours, minutes, seconds.
- Labeled one-time and recurring local alarms, editing, toggles, snooze, optional browser notifications.
- Four Web Audio synthesized soundscapes, synthesized chimes, master volume.
- Five Unsplash backgrounds, custom image URLs, 10/20/30-minute slideshow, blur and accent controls.
- Persistent notes, focus mode, keyboard shortcuts, reduced-motion support and mobile navigation.

## Behavior and browser requirements

Timer deadlines and stopwatch state persist across reloads. An overdue Pomodoro completes once when the app resumes, then starts the next session if auto-start is enabled; absent time does not create artificial completed sessions. Focus totals count completed work sessions, not skipped sessions.

The app must remain open and the device awake for reliable alarms and audible alerts. It is not a background OS alarm service. Browsers can delay callbacks in suspended tabs. Recurring alarms tolerate up to two minutes of callback delay. Audio begins after a click or keyboard interaction; saved soundscapes resume on a click. Browser notifications require permission and browser support, typically HTTPS or localhost.

Preferences, alarm schedules, notes, timer state, and daily statistics are stored in this browser's localStorage. Private browsing, storage clearing, or changing origin can remove or separate saved data. A visible notice appears when storage is unavailable. No user data is sent to an application backend. Unsplash photos and Google Fonts need network access; system fonts and an obsidian background provide fallbacks.

## Shortcuts

Space starts/pauses the selected timer, R resets it, L records a stopwatch lap, F toggles focus mode, and Escape dismisses overlays or exits focus mode. Typing fields retain their normal keyboard behavior.
