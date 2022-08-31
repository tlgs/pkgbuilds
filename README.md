# pkgbuilds

Packages I maintain for the [Arch User Repository](https://aur.archlinux.org/).

Some notes:

- Use [aurpublish](https://github.com/eli-schwartz/aurpublish) to help maintain
  multiple packages using git subtrees
- Run `namcap` on both the `PKGBUILD` and the resulting package archive
- Use `extra-x86_64-build` in lieu of `makepkg` to test a package
  (see [Building in a clean chroot](https://wiki.archlinux.org/title/DeveloperWiki:Building_in_a_clean_chroot))
