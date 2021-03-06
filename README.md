## NixOS-Config

This is a work in progress of my NixOS configuration.

## Installation
On NixOS, run `nixos-rebuild switch` to install the configuration specified here
and make it the boot default.

## dot-files
While I have tried to port dot-files over to a purely Nix config, xmonad (and
perhaps more applications in the future) is still configured via the dot file
specified in [my dot-files repo](https://github.com/blake-wilson/dot-files).

## Bootstrapping from fresh NixOS installation
* Install git `nix-env -i git`
* `cd /etc/nixos`
* `git init`
* `git remote add origin https://github.com/blake-wilson/nixos-config.git`
* `git fetch`
* `git checkout master`
* `git submodule init`
* `git submodule update`
* Test the system configuration via `nixos-rebuild test -I nixpkgs=nixpkgs-channels`
* Switch system configuration: `nixos-rebuild switch -I nixpkgs=nixpkgs-channels`
* `reboot`
