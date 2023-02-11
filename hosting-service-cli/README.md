oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g hosting-service-cli
$ decen-pub COMMAND
running command...
$ decen-pub (--version)
hosting-service-cli/0.0.0 darwin-x64 node-v18.11.0
$ decen-pub --help [COMMAND]
USAGE
  $ decen-pub COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`decen-pub hello PERSON`](#decen-pub-hello-person)
* [`decen-pub hello world`](#decen-pub-hello-world)
* [`decen-pub help [COMMANDS]`](#decen-pub-help-commands)
* [`decen-pub plugins`](#decen-pub-plugins)
* [`decen-pub plugins:install PLUGIN...`](#decen-pub-pluginsinstall-plugin)
* [`decen-pub plugins:inspect PLUGIN...`](#decen-pub-pluginsinspect-plugin)
* [`decen-pub plugins:install PLUGIN...`](#decen-pub-pluginsinstall-plugin-1)
* [`decen-pub plugins:link PLUGIN`](#decen-pub-pluginslink-plugin)
* [`decen-pub plugins:uninstall PLUGIN...`](#decen-pub-pluginsuninstall-plugin)
* [`decen-pub plugins:uninstall PLUGIN...`](#decen-pub-pluginsuninstall-plugin-1)
* [`decen-pub plugins:uninstall PLUGIN...`](#decen-pub-pluginsuninstall-plugin-2)
* [`decen-pub plugins update`](#decen-pub-plugins-update)

## `decen-pub hello PERSON`

Say hello

```
USAGE
  $ decen-pub hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/ShariqT/publishing-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `decen-pub hello world`

Say hello world

```
USAGE
  $ decen-pub hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ decen-pub hello world
  hello world! (./src/commands/hello/world.ts)
```

## `decen-pub help [COMMANDS]`

Display help for decen-pub.

```
USAGE
  $ decen-pub help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for decen-pub.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.2/src/commands/help.ts)_

## `decen-pub plugins`

List installed plugins.

```
USAGE
  $ decen-pub plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ decen-pub plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.3.0/src/commands/plugins/index.ts)_

## `decen-pub plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ decen-pub plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ decen-pub plugins add

EXAMPLES
  $ decen-pub plugins:install myplugin 

  $ decen-pub plugins:install https://github.com/someuser/someplugin

  $ decen-pub plugins:install someuser/someplugin
```

## `decen-pub plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ decen-pub plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ decen-pub plugins:inspect myplugin
```

## `decen-pub plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ decen-pub plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ decen-pub plugins add

EXAMPLES
  $ decen-pub plugins:install myplugin 

  $ decen-pub plugins:install https://github.com/someuser/someplugin

  $ decen-pub plugins:install someuser/someplugin
```

## `decen-pub plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ decen-pub plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ decen-pub plugins:link myplugin
```

## `decen-pub plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ decen-pub plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ decen-pub plugins unlink
  $ decen-pub plugins remove
```

## `decen-pub plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ decen-pub plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ decen-pub plugins unlink
  $ decen-pub plugins remove
```

## `decen-pub plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ decen-pub plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ decen-pub plugins unlink
  $ decen-pub plugins remove
```

## `decen-pub plugins update`

Update installed plugins.

```
USAGE
  $ decen-pub plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
