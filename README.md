# Remix Boilerplate
![Fleek 2024 Rebrand Boilerplate](https://github.com/fleek-tools/remix-template/assets/74613246/4dc6bab0-fb59-4953-8803-66143dec8a1a)


## 🚀 Project Structure

Inside of your Remix project, you'll see the following folders and files:

```
/
├── app/
│   ├── routes/
│   │   └── routes/
│   │   └── _index.tsx
│   ├── entry.client.tsx
│   ├── entry.server.tsx
│   └── root.tsx
├── public/
├── package.json
└── vite.config.json
```

Remix SSG works by wrapping the @remix-run/dev CLI and introducing a new plugin to modify the client runtime to fetch from static .json files. It then executes your handler to generate the static assets.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command         | Action                                       |
| :-------------- | :------------------------------------------- |
| `npm install`   | Installs dependencies                        |
| `npm run dev`   | Starts local dev server at `localhost:3000`  |
| `npm run build` | Build your production site to `./build/`     |
| `npm run start` | Preview your build locally, before deploying |

## ⚡ How to deploy to Fleek

### 1. Create a `fleek.json` config file:

You can configure this site deployment using [Fleek CLI]() and running:

```
 > fleek sites init
  WARN! Fleek CLI is in beta phase, use it under your own responsibility
   ? Choose one of the existing sites or create a new one. ›
    ❯ Create a new site
```

It will prompt you for a `name`, `dist` directory location & `build command`

- `name`: How you want to name the site
- `dist`: The output directory where the site is located, for this template it's `build`
- `build command`: Command to build your site, this will be used to deploy the latest version either by CLI or Github Actions

### 2. Deploy the site

After configuiring your `fleek.json` file, you can deployt the site by running

```
fleek sites deploy
```

After running it you will get an output like this:

```
 WARN! Fleek CLI is in beta, use it at your own discretion
  > Success! Deployed!
  > Site IPFS CID: QmP1nDyoHqSrRabwUSrxRV3DJqiKH7b9t1tpLcr1NTkm1M

  > You can visit through the gateway:
  > https://ipfs.io/ipfs/QmP1nDyoHqSrRabwUSrxRV3DJqiKH7b9t1tpLcr1NTkm1M
```

### Extra features

- **Continuous Integration (CI):** `fleek sites ci` [Documentation.](https://docs.fleek.xyz/services/sites/#continuous-integration-ci)
- **Adding custom domains:** `fleek domains create` [Documentation.](https://docs.fleek.xyz/services/domains/)

### Keep in mind:

This template has been configured to produce a static output using `remix-ssg` and `serve`.

You can find more information about static builds in [Remix Documentation](https://remix-ssg.pages.dev/docs/quick-start)

## 👀 Want to learn more?

Feel free to check [Remix documentation](https://remix.run/docs/en/main).
