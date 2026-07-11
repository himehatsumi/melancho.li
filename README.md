# melancho.li

The source for my small corner of the internet: a black-and-white personal homepage with my links and space reserved for Monogatari artwork.

It borrows the compact columns, one-pixel borders, and small labeled panels of old anime fan sites without trying to reproduce an old browser. There is not much machinery here on purpose: one static Astro page, no tracking, and one small clipboard script.

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

## Small details

- Email, Discord, and Matrix are marked as the most reliable ways to reach me.
- The Discord row copies my username because Discord does not provide a useful public profile link for a handle.
- The page uses system fonts and has no animation.
- Artwork slots are plain `IMAGE HERE` placeholders so the final images can be chosen later.

The site is intended for [melancho.li](https://melancho.li).

© 2026 himehatsumi. All rights reserved.
