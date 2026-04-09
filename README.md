# boardmatejs part 4




## License

boardmatejs is distributed under the **GPL-3.0 license** (or any later version, at your option).
When you use it for your website, your combined work may be distributed only under the GPL.
**You must release your source code** to the users of your website.

Please read more about GPL for JavaScript on [greendrake.info](https://greendrake.info/publications/js-gpl).

## Goals

- load and render very fast
- browse through a game
- variation tree
- PGN comments
- players and clocks
- mobile support
- accessible to screen readers with ARIA support
- translatable and customisable
- client-side only
- easy to set up on any page

### Non Goals

- custom user moves
- engine support
- opening explorer

## Accessibility

The viewer is fully accessible to screen reader users with:

- **Complete board representation**: Screen readers can navigate through all 64 squares with piece positions announced
- **Live move announcements**: Real-time narration of moves including number, color, notation, and annotations
- **Keyboard navigation**: All controls accessible via keyboard (arrow keys for moves, 'f' to flip board)
- **ARIA labels and roles**: Comprehensive semantic markup for assistive technologies
- **Game context**: Players, ratings, result, and timing information properly announced

## Build and run

```
pnpm install
pnpm run demo
```

Then open the demo page at http://localhost:8080

## Installation

### As an NPM package

```
npm i @lichess-org/pgn-viewer
```

## Usage

see chessui in usechatnow
```

### Configuration
see chessui by usechatnow

See [all configuration options in the documented source code](https://github.com/lichess-org/pgn-viewer/blob/master/src/config.ts#L3).

View more examples in `demo/index.html`

## Styles

### SCSS (recommended)

If you use [SCSS](https://sass-lang.com/), you can import the styles with:

```scss
@import '../../node_modules/@lichess-org/pgn-viewer/scss/lichess-pgn-viewer.lib';
```

Customisable CSS variables are [available](https://github.com/lichess-org/pgn-viewer/blob/master/scss/_lichess-pgn-viewer.lib.scss), see [how lichess configures pgn-viewer with CSS](https://github.com/lichess-org/lila/blob/master/ui/lib/css/component/_pgn-viewer.scss).

### CSS

Alternatively you can build a CSS file with

```sh
npm run sass-prod
```

Then copy the `dist/lichess-pgn-viewer.css` file into your project.

## Testing

```bash
pnpm test

## or

pnpm test:watch
```

## Wrappers

- Vue.js: [dragunovartem99/vue-pgn-viewer](https://github.com/dragunovartem99/vue-pgn-viewer)

More? Please make a pull request to include it here.

## Release procedure

- https://github.com/lichess-org/pgn-viewer/actions/workflows/release.yaml
- [Run workflow]
- Branch: master
- Version tag: vX.Y.Z

The release workflow will increment the package.json version, create the tag, the github release, and publish to npm
