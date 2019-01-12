# [Code::Stats](https://codestats.net/) plugin for [Zsh](http://www.zsh.org/)

## This a fork of the original [zsh-codestats plugin](https://github.com/dancek/zsh-codestats) Licensed to `Hannu Hartikainen`

[![GitHub tag](https://img.shields.io/github/tag/eendroroy/zsh-codestats.svg)](https://github.com/eendroroy/zsh-codestats/tags)

[![Contributors](https://img.shields.io/github/contributors/eendroroy/zsh-codestats.svg)](https://github.com/eendroroy/zsh-codestats/graphs/contributors)
[![GitHub last commit (branch)](https://img.shields.io/github/last-commit/eendroroy/zsh-codestats/master.svg)](https://github.com/eendroroy/zsh-codestats)
[![license](https://img.shields.io/github/license/eendroroy/zsh-codestats.svg)](https://github.com/eendroroy/zsh-codestats/blob/master/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/eendroroy/zsh-codestats.svg)](https://github.com/eendroroy/zsh-codestats/issues)
[![GitHub closed issues](https://img.shields.io/github/issues-closed/eendroroy/zsh-codestats.svg)](https://github.com/eendroroy/zsh-codestats/issues?q=is%3Aissue+is%3Aclosed)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/eendroroy/zsh-codestats.svg)](https://github.com/eendroroy/zsh-codestats/pulls)
[![GitHub closed pull requests](https://img.shields.io/github/issues-pr-closed/eendroroy/zsh-codestats.svg)](https://github.com/eendroroy/zsh-codestats/pulls?q=is%3Apr+is%3Aclosed)


zsh-codestats hooks onto Zsh, counts characters as you type and saves your statistics in Code::Stats. 
You'll receive XP for the following languages for each character you type.

- `Terminal (Zsh)`
- `Git`
- `Vagrant`
- `Docker`

## Installation

1. Ensure you have [`curl`](https://curl.haxx.se/).
1. Get your personal API key from https://codestats.net/my/machines and set environment variable in e.g. `.zshrc`.
    ```
    CODESTATS_API_KEY="<api key here>"
    ```
1. Install and source the script in one of the following ways (in `.zshrc` after the environment variable):

### Zplug

```
zplug "eendroroy/zsh-codestats"
```

Add a line for the plugin, run `zplug update`, then restart the shell by e.g. `exec zsh`.

### Manual installation

Clone this git repo and source the script directly.

```
source codestats.plugin.zsh
```

### Running on Windows Subsystem for Linux

If you are running Zsh on Windows and see this message:

```
_codestats_send_pulse:23: nice(5) failed: operation not permitted
```

This is caused due to WSL not supporting `nice` and Zsh using it by default for
backgrounded processes. As a workaround, in your `.zshrc`, set:

```
unsetopt BG_NICE
```

See the discussion in this related issue: https://github.com/Microsoft/WSL/issues/1887

## Options

- `CODESTATS_API_KEY`: the API key used when submitting pulses. Required.
- `CODESTATS_API_URL`: the base URL to the Code::Stats API. Only set this if you know what you're doing! :)
- `CODESTATS_LOG_FILE`: a log file for debugging. Must exist and be writable.

## Contributing

Bug reports and pull requests are welcome on GitHub at [zsh-codestats](https://github.com/eendroroy/zsh-codestats) repository.
This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

  1. Fork it ( https://github.com/eendroroy/zsh-codestats/fork )
  1. Create your feature branch (`git checkout -b my-new-feature`)
  1. Commit your changes (`git commit -am 'Add some feature'`)
  1. Push to the branch (`git push origin my-new-feature`)
  1. Create a new Pull Request

## Author

* **Hannu Hartikainen** - *Original Author* - [dancek](https://github.com/dancek)
* **indrajit** - *Owner* - [eendroroy](https://github.com/eendroroy)

## License

The project is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).