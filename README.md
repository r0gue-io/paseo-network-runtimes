# Paseo Releases
> ⚠️ NOTE: These builds are provided for development purposes only!

This repo provides cross-platform builds of the Paseo Network chain spec generator for usage with [`pop-cli`](https://github.com/r0gue-io/pop-cli) only.

Builds are generated as per the release tags at https://github.com/paseo-network/runtimes, along with any Rust compiler version noted within the release notes of each release.

The [workflow](./.github/workflows/release.yml) generates the cross-platform binaries and creates a corresponding release with the same release tag. The corresponding commit hash is added to the release notes for additional verification.

## Aura Signing Scheme
This repo also overrides the signing scheme used for Aura by the `asset-hub-paseo-runtime` runtime to standardise on 
SR25519 instead of ED25515 as found on Polkadot, easing integrations with SDK binaries and tooling.

## Supported Platforms
The currently supported platforms/targets are as follows:
- Linux
    - `aarch64-unknown-linux-gnu`
    - `x86_64-unknown-linux-gnu`
- macOS
    - `aarch64-apple-darwin`
    - `x86_64-apple-darwin`
