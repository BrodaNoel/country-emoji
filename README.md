# country-emoji
[![Build Status][travis_svg]][travis_url] [![Codeship Status for meeDamian/country-emoji][codeship_svg]][codeship_url] [![Coverage Status][coveralls_svg]][coveralls_url] [![codecov.io][codecov_svg]][codecov_url] [![npm version][npm_svg]][npm_url] [![XO code style][xo_svg]][xo_url] [![Dependency Status][dep_svg]][dep_url] [![devDependency Status][dev_dep_svg]][dev_dep_url]

[travis_svg]: https://travis-ci.org/meeDamian/country-emoji.svg?branch=master
[travis_url]: https://travis-ci.org/meeDamian/country-emoji
[codeship_svg]: https://app.codeship.com/projects/4c475430-6f94-0134-4dcc-3acc74581569/status?branch=master
[codeship_url]: https://app.codeship.com/projects/178069
[coveralls_svg]: https://coveralls.io/repos/github/meeDamian/country-emoji/badge.svg?branch=master
[coveralls_url]: https://coveralls.io/github/meeDamian/country-emoji?branch=master
[codecov_svg]: https://codecov.io/github/meeDamian/country-emoji/coverage.svg?branch=master
[codecov_url]: https://codecov.io/github/meeDamian/country-emoji?branch=master
[npm_svg]: https://badge.fury.io/js/country-emoji.svg
[npm_url]: https://badge.fury.io/js/country-emoji
[xo_svg]: https://img.shields.io/badge/code_style-XO-5ed9c7.svg
[xo_url]: https://github.com/sindresorhus/xo
[dep_svg]: https://david-dm.org/meeDamian/country-emoji.svg
[dep_url]: https://david-dm.org/meeDamian/country-emoji
[dev_dep_svg]: https://david-dm.org/meeDamian/country-emoji/dev-status.svg
[dev_dep_url]: https://david-dm.org/meeDamian/country-emoji#info=devDependencies

Converts between country names, ISO 3166-1 codes and flag emojis. **Has zero dependencies.**

## Install

```
$ npm install --save country-emoji
```

## Usage

```js
const {flag, code, name} = require('country-emoji');

flag('CL')
 // ~> 🇨🇱

code('🇨🇦')
 // ~> CA

name('🇶🇦')
 // ~> Qatar

// can extract name from string…
flag('Taiwan number one!')
 // ~> 🇹🇼

// …but only if there's no ambiguity
flag('Congo and Burma')
 // ~> undefined

flag('Republic of Tanzania')
 // ~> 🇹🇿

flag('Tanzania, United Republic of')
 // ~> 🇹🇿

code('Australia')
 // ~> AU

code('UAE')
 // ~> AE

name('AE')
 // ~> United Arab Emirates

code('UK')
 // ~> GB

// all values can be converted back and forth indefinitely
flag(name(flag(code(flag(name('NZ'))))))
 // ~> 🇳🇿
```

## Bugs and feedback

If you discover a bug please report it [here](https://github.com/meeDamian/country-emoji/issues/new).

Mail me at bugs@meedamian.com, or on twitter [@meeDamian](http://twitter.com/meedamian).

![codecov.io](https://codecov.io/github/meeDamian/country-emoji/branch.svg?branch=master)


## License

MIT @ [Damian Mee](https://meedamian.com)
