<p align="center">
  <img alt="Nimble logo" src="https://assets.nimblehq.co/logo/light/logo-light-text-320.png" />
</p>

---

Laptop is a script to set up an OS X laptop for web development.

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

The variant of the script in this branch is the script to set up a Macstadium machine for Github Actions Remote station.

## Requirements

We support:

* OS X Grand Sierra (10.13)
* OS X Mojave (10.14)
* OS X Catalina (10.15)

Older versions may work but aren't regularly tested. Bug reports for older
versions are welcome.

## Install

Download, review, then execute the script:

```bash
curl --remote-name https://raw.githubusercontent.com/nimblehq/laptop/feature/mac-stadium-github-action-remote/mac
bash zsh 2>&1 | tee ~/zsh.log
```

Restart the Terminal

```bash
less mac
bash mac 2>&1 | tee ~/laptop.log
```

### Set Up GitHub Actions

Follow the instruction for [Adding a self-hosted runner to an organization](https://docs.github.com/en/actions/hosting-your-own-runners/managing-self-hosted-runners/adding-self-hosted-runners#adding-a-self-hosted-runner-to-an-organization)

### Set Up Tart VM

```
bash tart
```

## What it sets up
### Default
* [Ruby] stable for writing general-purpose code
* [XCode] iOS IDE

[Ruby]: https://www.ruby-lang.org/en/
[XCode]: https://developer.apple.com/xcode/

## Debugging

Your last Laptop run will be saved to `~/laptop.log`.
Read through it to see if you can debug the issue yourself.
If not, copy the lines where the script failed into a
[new GitHub Issue](https://github.com/nimblehq/laptop/issues/new) for us.
Or, attach the whole log file as an attachment.

## Contributing

Edit the `mac` file.
Document in the `README.md` file.
Follow shell style guidelines by using [ShellCheck] and [Syntastic].

```sh
brew install shellcheck
```

[ShellCheck]: http://www.shellcheck.net/about.html
[Syntastic]: https://github.com/scrooloose/syntastic

## License

It is free software,
and may be redistributed under the terms specified in the [LICENSE] file.

[LICENSE]: LICENSE

## About

![Nimble](https://assets.nimblehq.co/logo/dark/logo-dark-text-160.png)

This project is maintained and funded by Nimble.

Inspired by the [project] of Thoughtbot.

We love open source and do our part in sharing our work with the community!
See [our other projects][community] or [hire our team][hire] to help build your product.

[project]: https://github.com/thoughtbot/laptop
[community]: https://github.com/nimblehq
[hire]: https://nimblehq.co/
