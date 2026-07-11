# melancho.li

The source for my small corner of the internet: a black-and-white personal homepage with my links and Monogatari artwork.

It borrows the compact columns, one-pixel borders, and small labeled panels of old anime fan sites without trying to reproduce an old browser. There is not much machinery here on purpose: one static Astro page with a single Firestore document for the shared hit counter.

## Running it

You will need Node.js 22.12 or newer.

```sh
npm install
npm run dev
```

Astro will print a local address, normally [http://localhost:4321](http://localhost:4321).

## Building it

```sh
npm run build
```

That creates the finished static site in `dist/`. To check that build locally:

```sh
npm run preview
```
though I don't see why you would do any of this. just visit it at https://melancho.li

## Firebase

The Firebase Hosting and Firestore files are already included. Do not run `firebase init` over them.

```sh
npm install -g firebase-tools
firebase login
firebase use --add
firebase deploy
```

The Hosting predeploy hook runs the Astro build automatically. Create the default Firestore database once before the first deployment.

## Small details

- Email, Discord, and Matrix are marked as the most reliable ways to reach me.
- The Discord row copies my username because Discord does not provide a useful public profile link for a handle.
- The page uses system fonts. Only the optional side quotes move, and they stop for reduced-motion settings.
- The artwork is served through Astro's image pipeline as optimized responsive WebP files.
- The unofficial AniList box reads public data from the AniList GraphQL API and keeps a verified static fallback.
- The hit counter is shared by everyone and increments once per browser session. Firestore stores only one total number, not visitor analytics.
- `firebase deploy` builds the Astro site, deploys it to Firebase Hosting, and publishes the counter rules.

The site is intended for [melancho.li](https://melancho.li).

## Image rights

Images from *Monogatari* belong to NISIOISIN and their respective copyright holders. They are used here for this personal fan site; no ownership is claimed.

© 2026 himehatsumi. All rights reserved.
