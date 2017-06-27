# OSX Limitations

There are some limitations in `networking` for `Docker fo mac` so we can not utilize full functionality of `--net="host"` command on top of that we are exporting some of the most common ports from container to the host machine

**Ports exposed**
80, 443, 3000, 3306, 3307, 3308, 8000, 8001, 8002, 8080, 9000

# Run commands without installing them

Simple way to run any executedble without installing it on your host machine.

# Requirements

Docker Engine

# Supported 

## Supported operating systems

- all unixes with kernel over [`master` branch]
- Docker for mac ( [`docker-for-mac`](../../tree/docker-for-mac) branch )
- Docker for mac edge [`docker-for-mac-edge` branch]

## Supported commands

- `node`
- `npm`
- `yarn`
- `php`

# Installation

Clone this repository.

```
git clone git@github.com:galileo/docker-binaries
```

Add `bin` directory to your executables.

You need to modify your `PATH` variable. So open `.bash_rc` or `.bash_profile` or any other file where you are storing your variables and add this entry

```
PATH=$PATH:{path_to_this_repository}/bin
```

> NOTE: For osx users there is a problem with `php`. As OSX comes with preinstalled version of `php` the `php` will not work. There is `run-php` alias command. More info [here](../../tree/docker-for-mac#limitations)

> NOTE 2: There are some limitations with the `Docker for mac` for networking features.

> NOTE 3: Please look into our [Docker for mac](../../tree/docker-for-mac) branch  for more information.

# Usage

## Prerequisites

You need to unistall your existing installations of commands that we provide you with this repo. Or you need to change the names for those command if you want to use both.

## Running commands

You can now run each of our commands.

```bash
npm -v && node -v && yarn -v && php -v
```

# Version swtich

We relay this functionality on top of oficial docker images so we can switch versions for each our command as we would like to use the docker tags.

To keep all usages as small as possible we are using as and distribution the smallests distributions, it can be `alpine` or in some cases `slim`.

For each supported command there is equivalent of DockerBinary environment variable. If you don't change the variable we are using always the `latest` available version.

## Using environemnt variables

```
TBD
```

# Resources

Article about how you can setup your own repository and how to install this one.
