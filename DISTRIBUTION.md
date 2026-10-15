# Segue distribution policy (proposed)

This public repository is for compiled Segue installers, checksum files, and
release notes only. Segue's development repository is private.

## What is currently licensed

**v2.4.4 and earlier downloads were distributed under MIT terms.** Preserve
the historical [MIT license](./LICENSE-MIT-LEGACY.md). Those permissions cannot
be canceled by later changes to the root LICENSE file.

## Before the first new proprietary version

- Review ownership, contribution history, and third-party license obligations.
- Confirm that the final DMG includes `License.txt` and that Segue.app contains
  `Contents/Resources/License.txt`.
- State clearly in the particular **new version's** release notes that the new
  version is free to use but proprietary and identify the applicable license.
- Publish only the reviewed Segue-<version>.dmg, SHA256SUMS.txt, and release
  notes. Do not upload source, private diagnostics, signing keys or music files.
- Publish from the **private developer Mac** with `bash macos/release-local.sh
  VERSION --publish` in `vinceservidad/segue`. The script uses the developer's
  local `gh auth login` credentials, not GitHub Actions or cloud runners.
  It requires successful local tests, packaged-app smoke checks, code-signing
  and disk-image validation, accurate release notes and a new version tag.
- Verify the checksum, signed app integrity, download, and fresh installation.
- Do not claim a build is Apple notarized without actually notarizing it.

## Limits

Compiled applications can be inspected or copied. A private source repository,
license restrictions, and brand protection reduce risk but cannot guarantee
that competitors will not make similar software. Historical MIT grants persist.

This policy requires review before a future release is published; it does not
alter the terms already granted for existing releases.

## Where new downloads come from

Segue is compiled locally on macOS from the private `vinceservidad/segue` repository.
Only the final `.dmg`, its checksum file, and release notes are uploaded
to this public repository. **No GitHub Actions are required.**

The `vX.Y.Z` release tags in this distribution repository point to its
public documentation, *not* the private application's Swift source. GitHub's
automatic source archives for these release tags therefore package only
the contents of this distribution repository.

This release channel still provides ad-hoc-signed, unnotarized builds.
Developer ID signing and Apple notarization require a separate Apple
Developer enrollment and signing process.
