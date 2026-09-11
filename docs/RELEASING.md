# GitHub setup and release checklist

## Repository profile

- Suggested name: `mila-codex-pet`
- Description: `Mila, a pixel-art Newfoundland companion for Codex, with installable assets and a pet-creation guide.`
- Suggested topics: `codex`, `virtual-pet`, `pixel-art`, `spritesheet`, `animation`, `newfoundland`
- Optional social preview: use a reviewed crop of the supplied contact sheet.

## Before the first public upload

- [ ] Review the README and character attribution.
- [ ] Choose a license, add its full text, and update `LICENSING.md` and the README.
- [ ] Confirm permission to publish the supplied artwork and previews.
- [ ] Create your GitHub repository and copy this kit's contents into its root, including the dotfiles and `.github` directory.
- [ ] Check that no local credentials, conversation exports, or agent scratch files are included.
- [ ] Test installation and note the actual operating system and Codex version below.

## Runtime verification record

Not yet performed for this repository kit. The supplied pet files were copied from an existing local installation.

When testing, record date, operating system, Codex version, installation result, animation result, and directional-look result here.

## Prepare a release

- [ ] Inspect every standard animation and all 16 look directions.
- [ ] Ensure preview media matches the atlas being released.
- [ ] Confirm `spriteVersionNumber: 2`, the relative atlas path, and 1536 × 2288 atlas dimensions.
- [ ] Move appropriate changelog entries into a dated version section.
- [ ] Create a ZIP containing `mila/pet.json` and `mila/spritesheet.webp`, preserving the `mila` directory.
- [ ] Create a release in GitHub with your chosen version, the ZIP, and the tested-platform notes.

Suggested first-release title: `Mila v1.0.0`. This package version is independent of sprite format version 2.

Suggested release summary:

> Meet Mila: a pixel-art Newfoundland companion with nine animation states and sixteen directional looks. Includes the installable pet package, visual previews, and a creation guide. See the README for installation and the release notes for tested environments.
