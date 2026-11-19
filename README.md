# releases

Update feeds and release notes for kysz.app apps, served at
<https://updates.kysz.app>. The apps themselves are closed source; this repo
only holds what installed copies read to update themselves.

| App | Feed | Downloads |
|---|---|---|
| Planotion | [`planotion/appcast.xml`](https://updates.kysz.app/planotion/appcast.xml) | releases tagged `planotion-v*` |
| Planotion Capture | [`capture/appcast.xml`](https://updates.kysz.app/capture/appcast.xml) | releases tagged `capture-v*` |

- `<app>/appcast.xml` is a [Sparkle](https://sparkle-project.org) feed. Every
  item is EdDSA-signed; edit it only through the app's release script, or the
  signatures stop matching.
- `<app>/notes/<version>.md` is that version's release notes, also embedded in
  the feed.
- Binaries are GitHub release assets, one release per version and app.

`.nojekyll` turns off GitHub Pages' Jekyll pass so files are served as-is.
