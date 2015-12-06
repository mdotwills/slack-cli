# slack-cli <sub><sup>| Slack on the command line via pure bash</sup></sub>
[![version](http://img.shields.io/badge/version-v0.1.0-blue.svg)](https://github.com/rockymadden/slack-cli/releases)
[![versioning](http://img.shields.io/badge/versioning-semver-blue.svg)](http://semver.org/)
[![branching](http://img.shields.io/badge/branching-github%20flow-blue.svg)](https://guides.github.com/introduction/flow/)
[![license](http://img.shields.io/badge/license-mit-blue.svg)](https://opensource.org/licenses/MIT)
[![status](http://img.shields.io/badge/status-working-brightgreen.svg)](#)

## Installation
```bash
$ brew tap rockymadden/rockymadden
$ brew install slack-cli
```
> __NOTE:__ Requires that your Slack team has one or more
[incoming webhook integrations](https://api.slack.com/incoming-webhooks)

## Usage

```bash
$ slack --help
Usage:
  slack init [--webhook|-w <webhook>] [--channel|-c <channel>] [--username|-u <username>] [--emoji|-e <emoji>] [--silent|-s]
  slack send [--message|-m <message>] [--webhook|-w <webhook>] [--channel|-c <channel>] [--username|-u <username>] [--emoji|-e <emoji>] [--silent|-s]

Settings Commands:
  init     Initialize default settings

Messaging Commands:
  send     Send a message
```
> __NOTE:__ All subcommands prompt for required arguments which were not provided via options. This
allows for both traditional option-based usage and also prompt-based usage.

### Initialize:

```bash
$ slack init
Enter default webhook (e.g. https://hooks.slack.com/services/XXX/XXX/XXX): https://hooks.slack.com/services/XXX/XXX/XXX
Enter default channel (e.g. @username): @username
Enter default username (e.g. username-bot): username-bot
Enter default emoji (e.g. :robot_face:): :robot_face:
Initializing: done
```

### Send a message:

```bash
$ slack send 'Hello World!'
Sending: done
```

```bash
$ slack send 'Hello World!' --channel='@username'
Sending: done
```

```bash
$ slack send
Enter message (e.g. Hello World!): Hello World!
Sending: done
```

```bash
$ slack send --channel='@username'
Enter message (e.g. Hello World!): Hello World!
Sending: done
```

## License
```
The MIT License (MIT)

Copyright (c) 2015 Rocky Madden (https://rockymadden.com/)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
