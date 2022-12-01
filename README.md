# Community Managed Token (CMT)

Community Managed Token is an exact 1:1 code deployment of the [spl_managed_token](https://github.com/solana-labs/solana-program-library/tree/master/managed-token) to support a full proxy of spl_token interfaces.

For composability purpose and follow the original spl_managed_token's philosophy, the goal of CMT is to  have a upstream_authority (usually from a upstream program's PDA) that controls the use cases of the token.

| Network | Program Address |
| ----------- | ----------- |
| Devnet  |    CMTQqjzH6Anr9XcPVt73EFDTjWkJWPzH7H6DtvhHcyzV |
| Mainnet |    CMTQqjzH6Anr9XcPVt73EFDTjWkJWPzH7H6DtvhHcyzV |

Entrypoints:
- InitializeMint
- InitializeAccount
- Transfer
- MintTo
- Burn
- CloseAccount
- Approve
- Revoke

## Build

```bash
# To build all on-chain programs
$ cargo build-sbf

# To build a specific on-chain program
$ cd <program_name>/program
$ cargo build-sbf
```

## Test

Unit tests contained within all projects can be run with:
```bash
$ cargo test      # <-- runs host-based tests
$ cargo test-sbf  # <-- runs BPF program tests
```

To run a specific program's tests, such as SPL Token:
```bash
$ cd <program_name>/program
$ cargo test      # <-- runs host-based tests
$ cargo test-sbf  # <-- runs BPF program tests
```

## License
Apache 2.0
