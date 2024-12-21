# Sablier Legacy [![CircleCI](https://circleci.com/gh/sablier-labs/legacy-contracts.svg?style=svg)](https://circleci.com/gh/sablier-labs/legacy-contracts) [![Coverage Status](https://coveralls.io/repos/github/sablier-labs/legacy-contracts/badge.svg?branch=develop)](https://coveralls.io/github/sablier-labs/legacy-contracts?branch=develop) [![Styled with Prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://prettier.io) [![Commitizen Friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/) [![License: LGPL3.0](https://img.shields.io/badge/License-LGPL%20v3-008033.svg)](https://opensource.org/licenses/lgpl-3.0)

This is the source code of the Sablier Legacy protocol, which has been superseded by [Sablier Lockup](https://github.com/sablier-labs/v2-core). For more details about how Sablier works, check out our docs at [docs.sablier.com](https://docs.sablier.com).

This repo is structured as a monorepo:

| Package                                                   | Description                                                       |
| --------------------------------------------------------- | ----------------------------------------------------------------- |
| [`@sablier/dev-utils`](/packages/dev-utils)               | Dev utils to be shared across Sablier projects and packages       |
| [`@sablier/protocol`](/packages/protocol)                 | The core token streaming protocol                                 |
| [`@sablier/shared-contracts`](/packages/shared-contracts) | Smart contracts to be shared across Sablier projects and packages |

## Usage :hammer_and_pick:

To compile the smart contracts, bootstrap the monorepo and open the package you'd like to work on. For example, here are the instructions for `@sablier/protocol`:

```bash
$ yarn run bootstrap
$ cd packages/protocol
$ truffle compile --all
$ truffle migrate --reset --network development
```

Alternatively, if you simply want to use the UI, head to
[legacy-recipient.sablier.com](https://legacy-recipient.sablier.com) to withdraw from streams.

## Contributing :raising_hand_woman:

Participation from the community is crucial for shaping the future development of Sablier. If you are interested in
contributing or have any questions, ping us on [Discord](https://discord.gg/KXajCXC).

We use [Yarn](https://yarnpkg.com/) as a dependency manager and [Truffle](https://github.com/trufflesuite/truffle)
as a development environment for compiling, testing, and deploying our contracts. The contracts were written in [Solidity](https://github.com/ethereum/solidity).

### Requirements

- yarn >=1.17.3
- truffle >= 5.0.35
- solidity 0.5.17

### Pre Requisites

Make sure you are using Yarn >=1.17.3.

```bash
$ npm install --global yarn
```

Then, install dependencies:

```bash
$ yarn install
```

### Watch

To re-build all packages on change:

```bash
$ yarn watch
```

### Clean

To clean all packages:

```bash
$ yarn clean
```

To clean a specific package:

```bash
$ PKG=@sablier/protocol yarn clean
```

### Lint

To lint all packages:

```bash
$ yarn lint
```

To lint a specific package:

```bash
$ PKG=@sablier/protocol yarn lint
```

### Prettier

To run prettier on all packages:

```bash
$ yarn prettier
```

Prettier cannot be run on individual packages.

### Test

To run all tests:

```bash
$ yarn test
```

To run tests in a specific package:

```bash
$ PKG=@sablier/protocol yarn test
```
