<div align="center">

<img src="https://raw.githubusercontent.com/HospitalRun/design/master/logo/logo-on-transparent.png" alt="HospitalRun logo"/>

![Last commit](https://img.shields.io/github/last-commit/hospitalrun/hospitalrun) [![Activity](https://img.shields.io/github/commit-activity/m/hospitalrun/hospitalrun)](https://github.com/hospitalrun/hospitalrun/pulse) ![Repo size](https://img.shields.io/github/repo-size/hospitalrun/hospitalrun) [![Slack](https://hospitalrun-slackin.herokuapp.com/badge.svg)](https://hospitalrun-slackin.herokuapp.com) [![Join the community on Spectrum](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/hospitalrun) [![MIT](https://badgen.net/github/license/HospitalRun/hospitalrun)](https://github.com/HospitalRun/hospitalrun/blob/master/LICENSE)

<hr />
</div>

All **HospitalRun** code lives in a single repository, an architecture generally called a monorepo. This repository holds all of HospitalRun's open source projects that lived in their own separate Github repos: [frontend](https://github.com/HospitalRun/hospitalrun-frontend), [server](https://github.com/HospitalRun/hospitalrun-server) and [components](https://github.com/HospitalRun/components).

## Table of Contents
 * [Toolchain & CLI](#toolchain--cli)
 * [Getting Started](#getting-started)
 * [Pull all submodules](#pull-all-submodules)
 * [Commiting](#commiting)
   * [How to commit a specific package?](#how-to-commit-a-specific-package) 
 * [Updating the monorepo structure](#updating-the-monorepo-structure)
 * [Docker Develop Env](#docker-develop-env)    

## Toolchain & CLI

We recommend the use of [**nvm**](https://github.com/nvm-sh/nvm#install--update-script) for the management of different versions of Node, and [**yarn**](https://yarnpkg.com/lang/en/docs/install/#mac-stable) for a fast, reliable, and secure dependency management. We suggest to install [**yarn**] with `npm i -g yarn`.

## Getting Started

Use these commands to start using the monorepo. The following commands require that your GitHub account has [SSH access](https://help.github.com/en/articles/connecting-to-github-with-ssh) enabled.

```
git clone git@github.com:HospitalRun/hospitalrun.git
cd hospitalrun
git submodule update --init --recursive
yarn
yarn workspaces run build

# Do some coding then commit with
npx git-cz

# Test the cli
npx hospitalrun --version
```

## Pull all submodules

Use these commands to update all submodules and use the last available commit.

```
git submodule update --recursive --remote

yarn upgrade // Update all dependencies automatically
yarn update // This is similar to npm-check interactive update mode. It provides an easy way to update outdated packages. 
```

## Commiting

This repo uses conventional commits. Commitizen is recommended for development. Once you have changes staged
you can run `git cz` from the root directory in order to commit to the proper standards.

1. Staging all pending changes. Es: `git add .`
2. Use the following command: `yarn commit`
3. Updates remote refs using local refs. Es: `git push` 

### How to commit a specific package?

```
yarn commit-frontend
yarn commit-server
yarn commit-components
yarn commit-cli
yarn commit-core
yarn commit-docs
```

You must follow the following rules:

1. Commit description must always start with a capital letter.
2. Always use a scope. Here are some examples:

**Generic**

```
setting
ci
deps
readme
devops
system
core
testing
cli
release
lifecycle
```

**Monorepo specific**

```
monorepo
package
release
lifecycle
workspace
```

## Updating the monorepo structure

Use these commands to add a new package after adding a submodule.

```
git submodule update --remote
git add ./packages
yarn upgrade
npx git-cz
```

## Docker Develop Env 

**WIP**

```
docker build -t hospitalrun .
docker-compose up
```



<hr />

# Behind HospitalRun

## Hosted by

[<img src="https://github.com/openjs-foundation/cross-project-council/blob/master/logos/openjsf-color.png?raw=true" width="120px;"/>](https://openjsf.org/projects/#atlarge)

## Sponsors

[![Sponsors](https://opencollective.com/hospitalrun/sponsors.svg?width=890)](https://opencollective.com/hospitalrun/contribute/sponsors-336/checkout)

## Backers

[![Backers](https://opencollective.com/hospitalrun/backers.svg?width=890)](https://opencollective.com/hospitalrun/contribute/backers-335/checkout)

## Lead Maintainer

[<img src="https://avatars2.githubusercontent.com/u/1620916?s=460&v=4" width="100px;"/><br /><sub><b>Maksim Sinik</b></sub>](https://github.com/fox1t)<br />

## Core Team

<!-- prettier-ignore -->
|[<img src="https://avatars1.githubusercontent.com/u/11684?s=460&v=4" width="100px;"/><br /><sub><b>Travis Boudreaux</b></sub>](https://github.com/tjboudreaux) | [<img src="https://avatars3.githubusercontent.com/u/25089405?s=460&v=4" width="100px;"/><br /><sub><b>Stefano Casasola</b></sub>](https://github.com/irvelervel) | [<img src="https://avatars3.githubusercontent.com/u/3400442?s=460&v=4" width="100px;"/><br /><sub><b>Michael J Feher</b></sub>](https://github.com/PhearZero) | [<img src="https://avatars1.githubusercontent.com/u/25009192?s=460&v=4" width="100px;"/><br /><sub><b>Riccardo Gulin</b></sub>](https://github.com/bazuzu666) | [<img src="https://avatars3.githubusercontent.com/u/18731800?s=460&v=4" width="100px;"/><br /><sub><b>Jack Meyer</b></sub>](https://github.com/jackcmeyer) | [<img src="https://avatars0.githubusercontent.com/u/6388707?s=460&v=4" width="100px;"/><br /><sub><b>Matteo Vivona</b></sub>](https://github.com/tehKapa) |
|---|---|---|---|---|---|

## Medical Supervisor

[<img src="https://avatars2.githubusercontent.com/u/24660474?s=460&v=4" width="100px;"/><br /><sub><b>M.D. Daniele Piccolo</b></sub>](https://it.linkedin.com/in/danielepiccolo)<br />

## Contributors

[![Contributors](https://opencollective.com/hospitalrun/contributors.svg?width=960&button=false)](https://github.com/HospitalRun/hospitalrun-frontend/graphs/contributors)

## Founders

<!-- prettier-ignore -->
| [<img src="https://avatars0.githubusercontent.com/u/609052?s=460&v=4" width="100px;"/><br /><sub><b>John Kleinschmidtr</b></sub>](https://github.com/jkleinsc) | [<img src="https://avatars0.githubusercontent.com/u/929261?s=400&v=4" width="100px;"/><br /><sub><b>Joel Worrall</b></sub>](https://github.com/tangollama)  | [<img src="https://avatars0.githubusercontent.com/u/1319791?s=460&v=4" width="100px;"/><br /><sub><b>Joel Glovier</b></sub>](https://github.com/jglovier)  |
|---|---|---|

# License

Released under the [MIT license](LICENSE).
