# pkgbuilds

Packages I maintain for the [Arch User Repository](https://aur.archlinux.org/).

Notes / checklist:

- Use [aurpublish](https://github.com/eli-schwartz/aurpublish) to help maintain
  multiple packages using git subtrees
- Use `extra-x86_64-build` in lieu of `makepkg` to test a package
  (see [Building in a clean chroot](https://wiki.archlinux.org/title/DeveloperWiki:Building_in_a_clean_chroot))
- Use `updpkgsums` to [generate new checksums](https://wiki.archlinux.org/title/Makepkg#Generate_new_checksums)
- Run `makepkg --printsrcinfo > .SRCINFO` to generate package metadata
  (redundant with aurpublish's hooks)
- Run `namcap` on both the `PKGBUILD` and the resulting package archive
  (redundant when using `extra-x86_64-build`)
