# Coachella + LA Itinerary

Plan the April 2027 trip in the browser. The app is a static website and saves
your plan in the current browser by default.

## Enable and open the website

The repository owner needs to enable Pages once:

1. Open [repository Pages settings](https://github.com/cw223322/Keira-Chloe-LA-Itinerary/settings/pages).
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Open the repository's **Actions** tab and rerun **Deploy static website to GitHub Pages**.

After the deployment workflow completes, visit:

<https://cw223322.github.io/Keira-Chloe-LA-Itinerary/>

To share a trip, use **Copy share link** in the app. Without Firebase configured,
the link opens the same room code but the saved data remains on each device.
To sync edits between devices, add a Firebase Realtime Database configuration
in the `FIREBASE_CONFIG` object in `index.html`.

## Run locally

From the project directory, run:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Stop the server with `Ctrl+C`.

## Publish updates

Push changes to the `main` branch. The GitHub Actions workflow deploys the
static site to GitHub Pages automatically. You can also run it manually from
the repository's **Actions** tab.
