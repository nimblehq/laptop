<p align="center">
  <img alt="Nimble logo" src="https://assets.nimblehq.co/logo/light/logo-light-text-320.png" />
</p>

---

Laptop is a script to set up an OS X laptop for web development.

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

## Requirements

We support:

- OS X Big Sur (11.6)
- OS X Monterey (12.3) both Apple Silicon and Intel

Older versions may work but aren't regularly tested. This script is tested on the most recent and its previous version.

## Install

Download, review, then execute the script:

```bash
curl --remote-name https://raw.githubusercontent.com/nimblehq/laptop/master/mac
less mac
bash mac 2>&1 | tee ~/laptop.log
```

Choose the additional packages when the prompts appear:

```
Do you want to install Web's dependencies? [y|N]
Do you want to install iOS's dependencies? [y|N]
Do you want to install Android's dependencies? [y|N]
```

## What it sets up

### Default

- [Ruby] stable for writing general-purpose code
- [Bundler] for managing Ruby libraries
- [Keybase] to have encrypted team communication
- [1Password] the world’s most-loved password manager
- [Slack] for general team communication
- [Google Chrome] as the default browser
- [Skitch] get your point across with fewer words using annotation, shapes and sketches
- [Postman] a collaboration platform for API development
- [iTerm2] a replacement for Terminal
- [git] distributed revision control system
- [Github CLI] GitHub’s official command line tool
- [Github Desktop] GitHub’s official GUI tool
- [Git Large File Storage] an open source Git extension for versioning large files
- [Homebrew] for managing operating system libraries
- [RVM] for managing versions of Ruby
- [NVM] for managing versions of Node.JS
- [Zsh] as your shell
- [oh-my-zsh] to spice up your shell
- [VS Code] code editor
- [gpg2] GNU Pretty Good Privacy (PGP) package
- [libyaml] YAML Parser
- [coreutils] GNU File, Shell, and Text utilities

[ruby]: https://www.ruby-lang.org/en/
[bundler]: http://bundler.io/
[keybase]: https://keybase.io/
[1password]: https://1password.com/
[slack]: https://www.slack.com/
[google chrome]: https://www.google.com/chrome/
[skitch]: https://evernote.com/products/skitch
[postman]: https://www.postman.com/
[iterm2]: https://www.iterm2.com/
[git]: https://git-scm.com
[github cli]: https://github.com/cli/cli
[github desktop]: https://desktop.github.com/
[git large file storage]: https://git-lfs.github.com/
[homebrew]: http://brew.sh/
[rvm]: https://rvm.io/
[nvm]: https://github.com/creationix/nvm
[zsh]: http://www.zsh.org/
[oh-my-zsh]: http://ohmyz.sh/
[vs code]: https://code.visualstudio.com/
[gpg2]: https://gnupg.org/
[libyaml]: https://github.com/yaml/libyaml
[coreutils]: https://www.gnu.org/software/coreutils

### Web

- [Go] programming language to build simple/reliable/efficient software
- [Elixir] functional metaprogramming aware language built on Erlang VM
- [Docker] for managing project dependencies
- [Heroku CLI] for interacting with the Heroku API
- [AWS CLI] official Amazon AWS command-line interface
- [ImageMagick] for cropping and resizing images
- [Postgres] for storing relational data
- [Yarn] JavaScript package manager
- [Phrase] for interacting with the Phrase API
- [JetBrains Toolbox] for managing JetBrains tools the easy way

[go]: https://golang.org
[elixir]: https://elixir-lang.org/
[docker]: https://www.docker.com/community-edition
[heroku cli]: https://toolbelt.heroku.com/
[aws cli]: https://aws.amazon.com/cli/
[imagemagick]: http://www.imagemagick.org/
[postgres]: http://www.postgresql.org/
[yarn]: https://yarnpkg.com/
[phrase]: https://phrase.com/cli/
[jetbrains toolbox]: https://www.jetbrains.com/toolbox-app/

### iOS

- [Cocoapods] a dependency manager for Cocoa projects
- [Figma] helps teams create, test, and ship better designs from start to finish
- [Proxyman] enables developers to observe and manipulate HTTP/HTTPS requests
- [Atlassian SourceTree] a free Git client for Mac
- [XCode] iOS IDE

[cocoapods]: https://cocoapods.org/
[figma]: https://www.figma.com/
[proxyman]: https://proxyman.io/
[atlassian sourcetree]: https://www.sourcetreeapp.com/
[xcode]: https://developer.apple.com/xcode/

### Android

- [Temurin] OpenJDK from the Adoptium
- [Android Studio] Android IDE
- [Android SDK] Software Development Kit for Android

[temurin]: https://adoptium.net
[android studio]: https://developer.android.com/studio/index.html
[android sdk]: https://developer.android.com/studio/releases/sdk-tools

It should take less than 15 minutes to install (depending on your machine and internet speed).

### M1 incompatible dependecies

- [Keybase] to have encrypted team communication

It will omit all these dependencies above while running the script in the M1 machines.

## Customize in `~/.laptop.local`

Your `~/.laptop.local` is run at the end of the Laptop script.
Put your customizations there.
For example:

```sh
#!/bin/sh

cask "dropbox"
cask "firefox"

brew "tree"
```

Write your customizations such that they can be run safely more than once.
See the `mac` script for examples.

Laptop functions such as `fancy_echo`,`brew_install_or_upgrade`,
and `gem_install_or_update` can be used in your `~/.laptop.local`.

See the [wiki](https://github.com/thoughtbot/laptop/wiki)
for more customization examples.

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

[shellcheck]: http://www.shellcheck.net/about.html
[syntastic]: https://github.com/scrooloose/syntastic

## License

It is free software,
and may be redistributed under the terms specified in the [LICENSE] file.

[license]: LICENSE

## About

![Nimble](https://assets.nimblehq.co/logo/dark/logo-dark-text-160.png)

This project is maintained and funded by Nimble.

Inspired by the [project] of Thoughtbot.

We love open source and do our part in sharing our work with the community!
See [our other projects][community] or [hire our team][hire] to help build your product.

[project]: https://github.com/thoughtbot/laptop
[community]: https://github.com/nimblehq
[hire]: https://nimblehq.co/
