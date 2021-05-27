## Projects

I made vue-p5, a Vue component. \
~85 github stars, ~300 dependent projects on Github, ~400 downloads/week. \
https://www.npmjs.com/package/vue-p5

I wrote two Telegram bots in Rust for myself and friends. [Ligmir]
pulls game character stats from dndbeyond.com using headless Chrome and
allows Telegram users to use those stats to roll dice.

I've set up infrastructure for my personal website at https://kinrany.dev/
(the one you're probably reading right now). The same DigitalOcean instance
hosts the bots (as Docker containers), with Caddy as reverse proxy.
The build processes are automated, and deployment is just one line.
The instance can also be replaced within 15 minutes.

Other things I did in Rust:

* Wrote a [nom] parser for reading public game logs for One Hour One Life: [Kinrany/one_hour_one_life](https://github.com/Kinrany/one_hour_one_life)
* Wrote a CLI for downloading stories from [instory.su] and converting them into [Ink] stories: [Kinrany/inkstory](https://github.com/Kinrany/inkstory)
* Changed Cargo so it can automatically format newly generated crates in workspaces: [rust-lang/cargo#7656](https://github.com/rust-lang/cargo/issues/7656)
* Contributed a minor refactoring to [Ruma], a [Matrix] reimplementation: [ruma/ruma#85](https://github.com/ruma/ruma/pull/85)
* Rewrote a friend's physics simulation (originally written in C)

Sometimes I start writing games, some of them are technically playable :)

[Ligmir]: https://github.com/Kinrany/ligmir/
[nom]: https://github.com/Geal/nom
[instory.su]: https://instory.su/
[Ink]: https://github.com/inkle/ink
[Ruma]: https://www.ruma.io/
[Matrix]: https://matrix.org/
