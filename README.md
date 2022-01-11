# Yay Chroot Shim

This is a set of scripts to allow building packages within chroots for Yay.

**WARNING**: this is just experimentation. The better approach would be to implement these
changes within Yay itself, but by using a shim, we might potentially be able to use this
as a standalone wrapper for makepkg + pacman itself.

## Rationale

While Arch is great at making sure everything is up to date in the core packages, there
can sometimes be problems.

The main one I've encountered is when a package needs `gcc>=11.2.0`, such as with `firefox-kde-opensource`.

It goes without saying, you should probably not install the experimental build of `gcc` as a system dependency.


Unfortunately, this means you have to build it yourself, and loose all the benefits of `yay`.