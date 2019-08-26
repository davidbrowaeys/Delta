delta
=====

delta deployment command for sfdx

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/delta.svg)](https://npmjs.org/package/delta)
[![Downloads/week](https://img.shields.io/npm/dw/delta.svg)](https://npmjs.org/package/delta)
[![License](https://img.shields.io/npm/l/delta.svg)](https://github.com/davidbrowaeys/delta/blob/master/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g delta
$ deloitte COMMAND
running command...
$ deloitte (-v|--version|version)
delta/0.0.1 darwin-x64 node-v10.16.0
$ deloitte --help [COMMAND]
USAGE
  $ deloitte COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`deloitte hello [FILE]`](#deloitte-hello-file)
* [`deloitte help [COMMAND]`](#deloitte-help-command)

## `deloitte hello [FILE]`

describe the command here

```
USAGE
  $ deloitte hello [FILE]

OPTIONS
  -f, --force
  -h, --help       show CLI help
  -n, --name=name  name to print

EXAMPLE
  $ deloitte hello
  hello world from ./src/hello.ts!
```

_See code: [src/commands/hello.ts](https://github.com/davidbrowaeys/delta/blob/v0.0.1/src/commands/hello.ts)_

## `deloitte help [COMMAND]`

display help for deloitte

```
USAGE
  $ deloitte help [COMMAND]

ARGUMENTS
  COMMAND  command to show help for

OPTIONS
  --all  see all commands in CLI
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v2.2.1/src/commands/help.ts)_
<!-- commandsstop -->
