# ICE Task 4 — Weather Dashboard UI

An Expo/React Native weather dashboard with hardcoded demonstration data for Johannesburg, Cape Town, and Durban.

## Project structure

```text
.
├── App.tsx              # Dashboard UI, weather data, and city selection
├── index.ts             # Expo entry point
├── app.json             # Expo application configuration
├── package.json         # Scripts and dependencies
├── package-lock.json    # Locked npm dependency versions
├── tsconfig.json        # TypeScript configuration
├── eslint.config.js     # Expo ESLint flat configuration
└── assets/              # Expo icon, splash, and favicon assets
```

## Run locally

```bash
npm ci
npm start
```

The available platform scripts are `npm run android`, `npm run ios`, and `npm run web`.

## Implemented dashboard behavior

- Selects Johannesburg, Cape Town, or Durban.
- Displays current conditions, weather details, a 24-hour forecast, a five-day forecast, and sun/moon information.
- Uses hardcoded demonstration data; it does not call a weather API.
- Uses remote Unsplash image URLs for the city hero backgrounds.

## Debugging and verification log

The following issues were verified by comparing the supplied `App.tsx` source with the repository and checking the current implementation:

| Issue | Current status |
| --- | --- |
| City buttons compared against the country instead of the city | Fixed; selection now stores and compares `weather.city`. |
| Humidity displayed the feels-like temperature | Fixed; humidity now uses `selectedWeather.humidity`. |
| Hourly cards all displayed the current temperature | Fixed; each card now uses `hour.temperature`. |
| Sunrise displayed the sunset value | Fixed; sunrise now uses `selectedWeather.sunrise`. |
| The 24-hour forecast was rendered vertically | Fixed; the nested forecast scroll is horizontal. |
| Five-day forecast layout and data rendering | Present in the current `App.tsx`. |

The repository history contains the related fixes in commits `81debe7`, `dcc5c9a`, and `353af33`.

Checks run on 2026-10-10:

- `npm ci` — completed successfully.
- `npm run lint` — passed.
- `npx tsc --noEmit` — passed.
- `npx expo-doctor` — passed all 18 checks.

There is no automated test suite in this repository, and no screenshot evidence was supplied. No runtime/device result or screenshot is claimed here.

## Scope notes

The assignment rubric was not included in the repository or the supplied conversation, so this README records only behavior and evidence that could be verified from the code, repository history, and local checks.
