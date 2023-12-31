# Git multiple user config manager

## Intall or Dev

```sh
git clone git@github.com:screw-hand/gum.git
cd gum
git remote add upstream git@github.com:gauseen/gum.git
git remote -vv
git fetch --all
git branch master upstream/master
pnpm i
pnpm link --global
# if you need the uninstall, Seel the #Uninstall chapter
```

# Uninstall

```sh
# Whether you use pnpm or pnm depends on how you install
(p)npm rm -g @screw-hand/gum
```

## Example

```sh
gum list

Currently used name=gauseen email=gauseen@gmail.com
┌────────────┬─────────┬─────────────────────────┐
│ group-name │    name │                   email │
├────────────┼─────────┼─────────────────────────┤
│    global  │ gauseen │ gauseen@gmail.com       │
│    user1   │ li si   │ lisi@gmail.com          │
│    user2   │ wang er │ wanger@gmail.com        │
└────────────┴─────────┴─────────────────────────┘
```

```sh
gum use user1

Currently used name=li si email=lisi@gmail.com
```

## Usage

```sh
Usage: gum [options] [command]

Options:
  -V, --version                 output the version number
  -h, --help                    display help for command

Commands:
  list|ls                       List all the user config group
  set|s [options] <group-name>  Set one group for user config
  use|u [options] <group-name>  Use one group name for user config
  delete|del <group-name>       Delete one group
  help [command]                display help for command
```

## Change Log

### v1.0.6

- feat: Suport `gum list` use show the 
- feat: Suport alias command

### v1.0.5

- feat: Support `gum use <group-name> --global` commands that are not Git repositories

### v1.0.4

- fix: support user.name contain space

### v1.0.3

- fix: Group name can't be 'global'

### v1.0.2

- feat: `gum --version` cmd
- fix: support node v9.0.0
