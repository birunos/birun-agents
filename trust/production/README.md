# Production Repository Trust

This directory contains public trust material for production BirunOS agent
repository releases. It must never contain private keys.

`release-1.pub` is the raw lowercase-hex Ed25519 public key for the delegated
online release signer. Its private key is stored as the
`BIRUN_REPOSITORY_RELEASE_1_KEY_PEM_B64` secret in the reviewer-protected
`production-repository` GitHub environment.

The release key currently has no production authority. Before it can sign a
production release, the offline root ceremony must add:

- `root.json`, signed by the required threshold of offline root custodians; and
- `trust-root.json`, containing the corresponding root public keys for the
  BirunOS image.

The root document must delegate `release-1` and exactly match
`release-1.pub`. Follow the ceremony and publication procedure in the BirunOS
repository at `docs/operations/production-repository-signing.md`.

Do not publish a `prod` release tag or change the BirunOS default repository
configuration until the root ceremony, signed-bundle dry run, independent
fingerprint review, and device rollout checks have passed.
