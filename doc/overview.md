@copyright 2018 Ilya Khaprov <<i.khaprov@gmail.com>>.
@title lazy_supervisor
@version 0.0.1

@doc

[![Hex.pm][Hex badge]][Hex link]
[![Hex.pm Downloads][Hex downloads badge]][Hex link]
[![Build Status][Travis badge]][Travis link]
[![Coverage Status][Coveralls badge]][Coveralls link]

## Lazy supervisor

Just like standard OTP but lazy(so lazy it's a copy-pasta):
 - stops children started by `start_children` after a timeout;
 - also stops child started by `start_children` if the calling process stops.

Example - one-off connection in a separate process and you don't want to wait forever, plus after you
stopped waiting this connection is useless anyway.

## Contributing

Section order:

- Types
- Macros
- Callbacks
- Public API
- Deprecations
- Private Parts

Install the `git' pre-commit hook:

<pre lang="bash">
./bin/pre-commit.sh install
</pre>

The pre-commit check can be skipped by passing `--no-verify' to `git commit'.

## License

MIT

<!-- Named Links -->

[Hex badge]: https://img.shields.io/hexpm/v/lazy_supervisor.svg?maxAge=2592000?style=plastic
[Hex link]: https://hex.pm/packages/lazy_supervisor
[Hex downloads badge]: https://img.shields.io/hexpm/dt/lazy_supervisor.svg?maxAge=2592000
[Travis badge]: https://travis-ci.org/deadtrickster/lazy_supervisor.svg?branch=version-3
[Travis link]: https://travis-ci.org/deadtrickster/lazy_supervisor
[Coveralls badge]: https://coveralls.io/repos/github/deadtrickster/lazy_supervisor/badge.svg?branch=master
[Coveralls link]: https://coveralls.io/github/deadtrickster/lazy_supervisor?branch=master
