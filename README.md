# enveigle

Deceive Ansible to template Trellis .env files to local Bedrock

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/enveigle.svg)](https://npmjs.org/package/enveigle)
[![Downloads/week](https://img.shields.io/npm/dw/enveigle.svg)](https://npmjs.org/package/enveigle)
[![License](https://img.shields.io/npm/l/enveigle.svg)](https://github.com/ItinerisLtd/enveigle/blob/master/package.json)
[![Hire Itineris](https://img.shields.io/badge/Hire-Itineris-ff69b4.svg)](https://www.itineris.co.uk/contact/)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Goal](#goal)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [FAQ](#faq)
  - [Can I run `$ npx enveigle` instead?](#can-i-run--npx-enveigle-instead)
  - [Nothing happen after running the command?](#nothing-happen-after-running-the-command)
  - [Why not commit `enveigle.yml` under git?](#why-not-commit-enveigleyml-under-git)
  - [It looks awesome. Where can I find some more goodies like this?](#it-looks-awesome-where-can-i-find-some-more-goodies-like-this)
  - [This isn't on wp.org. Where can I give a ⭐️⭐️⭐️⭐️⭐️ review?](#this-isnt-on-wporg-where-can-i-give-a-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F-review)
- [Feedback](#feedback)
- [Security](#security)
- [Change log](#change-log)
- [Credits](#credits)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Goal

Populate `.env` files to local Bedrock with ansible so that we can develop with [valet](https://roots.io/guides/wordpress-local-development-on-os-x-with-valet-and-bedrock/) instead of vagrant while keeping [ansible vault](https://roots.io/trellis/docs/vault/), [wordpress_env_defaults](https://github.com/roots/trellis/blob/834966fc73f3524974d77d0d7078e73ef76c3eef/roles/deploy/vars/main.yml#L1) and all ansible goodies.

## Requirements

- Trellis
- Bedrock
- Anisble v2 or later
- NodeJS v10.13.0 or later

## Installation

```sh-session
$ yarn global add @itinerisltd/enveigle
```

## Usage

```sh-session
$ cd /path/to/trellis

# For normal Trellis setup, i.e: `--env=development`
$ enveigle

# For brave developers
$ enveigle --env=my-custom-dev-env

# For the confused
$ enveigle --help
Deceive Ansible to template Trellis .env files to local system

USAGE
  $ enveigle

OPTIONS
  -e, --env=env  [default: development] local environment name
  -h, --help     show CLI help
  -v, --version  show CLI version
```

## FAQ

### Can I run `$ npx enveigle` instead?

Why not?

### Nothing happen after running the command?

By default, Trellis name the local environment `development`.
If you change it or passing an incorrect `--env` flag, the [anisble playbook](./templates/enveigle.yml) skip without showing errors.

This is not ideal. Pull requests are welcomed.

### Why not commit `enveigle.yml` under git?

Because we have too [many sites to maintain](https://www.itineris.co.uk/work/), adding/updating [`enveigle.yml`](./templates/enveigle.yml) to all of our sites is tedious.

### It looks awesome. Where can I find some more goodies like this?

- Articles on [Itineris' blog](https://www.itineris.co.uk/blog/)
- More projects on [Itineris' GitHub profile](https://github.com/itinerisltd)
- Follow [@itineris_ltd](https://twitter.com/itineris_ltd) and [@TangRufus](https://twitter.com/tangrufus) on Twitter
- Hire [Itineris](https://www.itineris.co.uk/services/) to build your next awesome site

### This isn't on wp.org. Where can I give a ⭐️⭐️⭐️⭐️⭐️ review?

Thanks! Glad you like it. It's important to make my boss know somebody is using this project. Instead of giving reviews on wp.org, consider:

- tweet something good with mentioning [@itineris_ltd](https://twitter.com/itineris_ltd) and [@TangRufus](https://twitter.com/tangrufus)
- star this [Github repo](https://github.com/ItinerisLtd/enveigle)
- watch this [Github repo](https://github.com/ItinerisLtd/enveigle)
- write blog posts
- submit pull requests
- [hire Itineris](https://www.itineris.co.uk/services/)

## Feedback

**Please provide feedback!** We want to make this library useful in as many projects as possible.
Please submit an [issue](https://github.com/ItinerisLtd/enveigle/issues/new) and point out what you do and don't like, or fork the project and make suggestions.
**No issue is too small.**

## Security

If you discover any security related issues, please email [hello@itineris.co.uk](mailto:hello@itineris.co.uk) instead of using the issue tracker.

## Change log

Please see [CHANGELOG](./CHANGELOG.md) for more information on what has changed recently.

## Credits

[enveigle](https://github.com/ItinerisLtd/enveigle) is a [Itineris Limited](https://www.itineris.co.uk/) project created by [Tang Rufus](https://typist.tech).

Full list of contributors can be found [here](https://github.com/ItinerisLtd/enveigle/graphs/contributors).

## License

[enveigle](https://github.com/ItinerisLtd/enveigle) is released under the [MIT License](https://opensource.org/licenses/MIT).
