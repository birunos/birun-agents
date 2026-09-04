# Development Repository Trust

This directory contains public trust material for development-only BirunOS
agent repository candidates. It must never contain private keys.

`root-1.pub` and `release-1.pub` are raw DER Ed25519 public keys. Their private
keys are stored as environment secrets in the `development-repository` GitHub
environment. This online 1-of-1 root is intentionally convenient for active
development and does not meet the production custody requirements.

Development candidates must use an unmistakable development tag, remain out of
the BirunOS default repository configuration, and be replaceable without a
device migration promise. Production releases continue to require the separate
offline threshold-root ceremony documented under `trust/production`.
