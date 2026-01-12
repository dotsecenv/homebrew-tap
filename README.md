# dotsecenv Homebrew Tap

[![Homebrew install](https://github.com/dotsecenv/homebrew-tap/actions/workflows/post-release.yml/badge.svg)](https://github.com/dotsecenv/homebrew-tap/actions/workflows/post-release.yml)

This is the official Homebrew tap for [dotsecenv](https://dotsecenv.com).

## Installation

Add the tap and install:

```bash
brew tap dotsecenv/tap
brew install dotsecenv
```

## Code Signing and Notarization

All macOS binaries are:

- **Code-signed** with an Apple Developer ID certificate
- **Notarized** by Apple for Gatekeeper compatibility

The Homebrew cask automatically removes the quarantine attribute during installation, so you won't see Gatekeeper warnings.

### Verifying the Signature

You can verify the code signature and notarization status:

```bash
# Verify code signature
codesign --verify --verbose "$(brew --prefix)/bin/dotsecenv"
# Expected: valid on disk

# Verify notarization status
spctl --assess --verbose "$(brew --prefix)/bin/dotsecenv"
# Expected: accepted
# source=Notarized Developer ID
```

## Documentation

For more information, see the [main repository](https://github.com/dotsecenv/dotsecenv).
