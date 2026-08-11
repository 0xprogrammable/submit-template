# Review and activation

## Status model

Application, release, and availability are separate facts. A state is recorded only when its own requirements are met.

Application states are `Draft`, `Submitted`, `Under review`, `Changes requested`, `Accepted`, `Withdrawn`, `Rejected`, and `Superseded`.

- **Draft** means the creator is still preparing the package.
- **Submitted** means one exact revision entered intake.
- **Under review** means evidence is being checked. It is not approval.
- **Changes requested** means the same revision is not ready. A source change creates a new target.
- **Accepted** means the exact review target passed the published review policy.
- **Withdrawn** means the submitter ended the application.
- **Rejected** means the exact review target did not satisfy the published policy.
- **Superseded** means a newer application replaced the recorded target.

Release states are `Undeployed`, `Deployed`, `Verified`, and `Activated`.

- **Undeployed** means no finalized deployment is recorded for the accepted version.
- **Deployed** means a finalized deployment exists at the recorded chain and address.
- **Verified** means source, artifacts, and runtime code correspond to the accepted version.
- **Activated** means the recorded authority permits the exact version to be selected for new launches.

Availability is `Unavailable`, `Available`, `Suspended`, or `Retired`.

- **Unavailable** means the public product surface cannot prepare a launch for the version.
- **Available** means the product surface can prepare a launch, subject to current per-launch checks.
- **Suspended** means new launches are temporarily blocked while existing onchain records remain unchanged.
- **Retired** means the version remains historical but cannot be selected for a new launch.

## Version boundary

Acceptance never follows a moving branch. It binds one repository, commit, tree, chain ID, artifact set, runtime identities, fee policy, payout identity, factory, launch profile, dependency set, and parameter envelope.

Any material change creates a new version. Existing launches remain attached to the version they used.

## Per-launch checks

An active template does not authorize arbitrary launches. Before each transaction, Programmable checks:

- the template version is still active;
- deployed code and authorities still match the recorded version;
- user inputs remain inside the approved boundaries;
- wallet, chain, nonce, salt, and target addresses are current;
- fees and recipients match the active policy;
- simulation and provider health meet the launch profile requirements; and
- the launch has not already been consumed or replayed.

These checks should complete during the launch flow. They do not require a new human review when the version and inputs remain unchanged.

If any required check fails or is unavailable, no transaction may be prepared or submitted. Time-sensitive bindings must be checked again immediately before execution.

## Suspension and retirement

Once implemented, the recorded suspension authority may block new launches for an exact version through the published control path. The resulting state, reason, and effective time or block must be recorded. Until then, suspension and retirement are planned policy states, not active controls. This does not rewrite or disable contracts and pools that already exist.

A retired version remains part of the historical record but cannot be selected for a new launch.
