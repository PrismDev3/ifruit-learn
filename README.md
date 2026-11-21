# iFruit OS — Public Build Links

iFruit OS is a browser-based desktop simulation inspired by the iFruit universe. It is a website, not a real operating system.

## Run the hosted demo

- [Launch iFruit OS on GitHub Pages](https://prismdev3.github.io/ifruit-learn/learn-1.html) — the run URL includes “learn”.
- Demo lock-screen password: `jamesisawesome`
- [SVG demo](https://prismdev3.github.io/ifruit-learn/learn-1.svg) — open it as a standalone page.
- [Public link hub](https://prismdev3.github.io/ifruit-learn/)

## Build files and CDN links

CDN endpoints below expose the HTML/SVG files as file content. Use the GitHub Pages link above to run the application.

| Format | HTML file | SVG file |
| --- | --- | --- |
| jsDelivr | [View HTML source](https://cdn.jsdelivr.net/gh/PrismDev3/ifruit-learn@main/learn-1.html) | [View SVG source](https://cdn.jsdelivr.net/gh/PrismDev3/ifruit-learn@main/learn-1.svg) |
| GitHub raw | [View HTML source](https://raw.githubusercontent.com/PrismDev3/ifruit-learn/main/learn-1.html) | [View SVG source](https://raw.githubusercontent.com/PrismDev3/ifruit-learn/main/learn-1.svg) |
| Githack | [View HTML source](https://raw.githack.com/PrismDev3/ifruit-learn/main/learn-1.html) | [View SVG source](https://raw.githack.com/PrismDev3/ifruit-learn/main/learn-1.svg) |
| Statically | [View HTML source](https://statically.io/gh/PrismDev3/ifruit-learn/main/learn-1.html) | [View SVG source](https://statically.io/gh/PrismDev3/ifruit-learn/main/learn-1.svg) |

- [Build repository](https://github.com/PrismDev3/ifruit-learn)

## Render

[Deploy the Render static site](https://render.com/deploy?repo=https%3A%2F%2Fgithub.com%2FPrismDev3%2Fifruit-learn). The blueprint is ready; sign-in and deployment confirmation are required. Render assigns an `onrender.com` URL after deployment.

## ESM package modules

These are JavaScript import URLs for developers. The app's standalone build already bundles its dependencies.

- [React](https://esm.sh/react@19.3.1)
- [React DOM client](https://esm.sh/react-dom@19.3.1/client)
- [Motion](https://esm.sh/motion@14.14.0/react)
- [Lucide React](https://esm.sh/lucide-react@1.76.0)

The standalone files bundle the app shell. The full local game and media asset library is not included in this small public build, so some previews and games may need their original hosts or a full asset deployment.

## License

The source code is MIT licensed. Third-party game builds, artwork, posters, and media remain subject to their respective licenses.