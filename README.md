# pkgbuilds

Packages I maintain for the [Arch User Repository](https://aur.archlinux.org/).

Notes / checklist:

- Make whichever changes are required to the relevant `PKGBUILD`
- Use `updpkgsums` to automatically
  [generate new checksums](https://wiki.archlinux.org/title/Makepkg#Generate_new_checksums)
- Use `extra-x86_64-build` in lieu of `makepkg` to test a package
  (see [Building in a clean chroot](https://wiki.archlinux.org/title/DeveloperWiki:Building_in_a_clean_chroot))
- Run `makepkg --printsrcinfo > .SRCINFO` to generate package metadata
  (redundant with aurpublish's hooks)
- Run `namcap` on both the `PKGBUILD` and the resulting package archive
  (redundant when using `extra-x86_64-build`)
- Use [aurpublish](https://github.com/eli-schwartz/aurpublish) to help maintain
  multiple packages using git subtrees
