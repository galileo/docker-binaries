# Run all your code within container

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
- `php`

# Installation

Clone this repository.

```
TBD
```

Add `bin` directory to your executables.

```
TBD
```

> NOTE: For osx users there is a problem with `php`. As OSX comes with preinstalled version of `php` the `php` will not work. There is alias command for you you can call `phpx`.

# Usage

You can now run each of our commands.

```bash
npm -v && node -v && php -v
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
