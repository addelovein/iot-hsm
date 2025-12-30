# Changes

## YubiKey PKCS#11 parity with SoftHSM
- Generate keypair uses YubiKey PIV slots and maps object IDs to slots.
- RSA 4096 rejected for YubiKey PIV; RSA 2048 and EC P-256/P-384 allowed.
- Self-signed cert flow uses pin fallback when signpin is not provided.
- Import certificate for YubiKey uses yubico-piv-tool and slot mapping.
- Delete/clear slot for YubiKey deletes key and certificate using management key.

## API/UI updates
- Wizard key generation passes management key for YubiKey.
- Clear Slot forces a slot refresh to avoid stale UI state.
- Expert UI includes Management Key field for YubiKey key generation.

