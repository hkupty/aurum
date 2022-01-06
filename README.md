# Aurum

> gold (Au), chemical element, a dense lustrous yellow precious metal of Group 11 (Ib), Period 6, of the periodic table.
[Britannica](https://www.britannica.com/science/gold-chemical-element)

## Why

I used to have an AUR helper that I wrote over the course of many years, always improving a little bit, but I was growing tired of its manual workflow.

So I decided to use something that:
* Relied solely on AUR's [RPC Interface](https://wiki.archlinux.org/title/Aurweb_RPC_interface);
* Was simple, easy to read the source and understand (since I usually improve it from time to time);
* Didn't require manual work from me (i.e. searching the packages, cloning the repo);
* In fact, I didn't want it to rely on the git structure of the aur packages:
  * Whenever I manually updated the files, I got conflicts;
  * Whenever `-git` packages auto-updated their own versions, I got conflicts;
  * I had two sources of truth (pacman database and the git directory) to know which packages I cared about;

All in all, it was a good opportunity for me to rethink my workflow.

## Cool, I want to try

Download/clone this repo, `cd ~/.local/bin`, `ln -s <your path to aurum>/bin/aurum`.

Optionally, you can ln it to `au` instead of `aurum` since that's shorter and still correct.

## I love it, want to contribute

The to-do list sits in the bin script. Sorry, hackish 1-person project.
But overall, I plan on doing the following:
* Porting to a higher level language (clojure + [babashka](https://github.com/babashka/babashka) seems like the choice for me);
* Add a little bit of config;
* Use `XDG_CACHE` to persist built packages as well as build folders;
* Allow for adding patches and/or updating the `PKGBUILD` file before building;
* Add search;
* Reduce number of HTTP calls when checking versions by performing a single search w/ all items and iterating through the results (might be done after porting to another language).

### That seems too much but I still want to help

Consider [sponsoring me](https://github.com/sponsors/hkupty) :)
