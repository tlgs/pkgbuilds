# pkgbuilds

Packages I maintain for the [Arch User Repository](https://aur.archlinux.org/).
Uses [aurpublish](https://github.com/eli-schwartz/aurpublish).

Checklist:

- Make whichever changes are required to the relevant `PKGBUILD`
- Use `updpkgsums` to automatically
  [generate new checksums](https://wiki.archlinux.org/title/Makepkg#Generate_new_checksums)
- Use `extra-x86_64-build` in lieu of `makepkg` to build/test a package
  (see [Building in a clean chroot](https://wiki.archlinux.org/title/DeveloperWiki:Building_in_a_clean_chroot))
- Install resulting package with `pacman -U`. Make sure it runs!
- Stage and commit changes to `PKGBUILD`
- Run `aurpublish $PACKAGE` to push to the AUR

Notes:

- aurpublish's hooks generate package metadata and update `.SRCINFO`
  (i.e. `makepkg --printsrcinfo > .SRCINFO`)
- `extra-x86_64-build` automatically runs `namcap` on the `PKGBUILD`
  and resulting package archive
