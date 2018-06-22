# npm-autorelease

Based on [npm-release][n-r] by Tom Ashworth, this script will:

- Automatically bump the version in `package.json`
- Commit 'chore(release): Release vX.X.X-X'
- Tag your release
- Push the commit & tag (`git push && git push --tags`)
- Release to npm (with `npm publish`)

Versioning is based on commit messages since the last release. Commits should be using the [AngularJS Commit Guidelines][a-g], as this package will use the type of the commits to decide the next version.

## Install

`npm install -g npm-autorelease`

## Usage

You must use `npm-autorelease` in a folder with a `package.json` and a remote to push to.

You may also set the following environment variables (useful for CI Pipeline tools)

- `GIT_USER` - A user to push the release and tags under
- `GIT_PASS` - A token or password for the user

## Options

- `--dry-run` - Output only the recommended release type for the current repo without applying any commits, tags or releases to your project.

## License

MIT

[s-r]: https://github.com/semantic-release/semantic-release
[n-r]: https://github.com/tgvashworth/npm-release
[a-g]: https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#
