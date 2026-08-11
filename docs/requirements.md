# Template requirements

These requirements define the minimum review package for one reusable template version. They do not open public intake by themselves.

## Source and rights

- The complete source is available in a public GitHub repository.
- The application binds the numeric repository ID, full commit, and tree.
- Dependencies are pinned and their licenses are disclosed.
- The submitter owns the source or has permission to publish and submit it.
- The source has an explicit license. A public repository without a license is not enough.

## Reproducible build

- Build commands work from a clean checkout.
- Compiler, package manager, dependency, and configuration versions are pinned.
- Creation code and runtime code hashes are recorded for every deployed contract.
- Generated files can be reproduced or are explicitly identified as reviewed inputs.

## Template behavior

- The product behavior is described in plain language.
- Every hook permission and callback is documented.
- Asset, fee, custody, liquidity, claim, and exit flows are complete.
- Failure behavior is defined for unavailable providers, stale data, reverts, and partial execution.
- Upgradeability, pause controls, privileged roles, and external dependencies are disclosed.

## Creator inputs

- Every configurable field has a type, description, and hard boundary.
- Unsafe combinations are rejected before a transaction is prepared.
- Inputs cannot select arbitrary targets, selectors, delegate calls, or unbounded external code.
- Fee, beneficiary, quote asset, pool, supply, and authority rules are explicit.

## Tests and security evidence

- Unit and integration tests cover intended behavior and failure paths.
- Fuzz or invariant tests cover value conservation and bounded configuration where applicable.
- A threat model covers callback authentication, reentrancy, denial of service, price manipulation, custody, and privileged actions.
- Candidate rehearsal evidence is bound to the exact reviewed version. Official deployment and source verification remain later release states.
- Unknown evidence remains pending. A local pass is not an independent audit.

## Fee and payout

- The exact fee basis, denomination, event, accumulator, claim path, and recipient are documented.
- The creator payout address is explicit and supports the required chain.
- Accrued creator revenue cannot be redirected by changing a future template version.
- The Programmable and creator shares are separate liabilities.
- A payout address change creates a new reviewed version unless the accepted version already binds the exact migration mechanism and authority, and the current migration verifies that recorded binding.

## Launch compatibility

- The template uses an active Programmable launch profile.
- Deployment and initialization can be executed and verified within production limits.
- The resulting token, hook, pool, and supporting contracts can be identified onchain.
- A launch can be stamped, finalized, indexed, and displayed without relying on names or offchain claims.
- Each launch can be checked against the active template version and allowed parameter envelope.

## Application hygiene

- No secrets, private URLs, personal data, or unrelated files are included.
- All claims cite exact evidence.
- Missing, blocked, failed, and passed checks remain separate.
- Review, deployment, activation, and public availability remain separate states.
