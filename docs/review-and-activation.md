# Review and activation

## Lifecycle

Possible states are `Draft`, `Submitted`, `Under review`, `Changes requested`, `Accepted`, `Deployed`, `Activated`, and `Available`. Later states occur only when their own requirements are met.

Each state has a different meaning:

- **Draft** means the creator is still preparing the package.
- **Submitted** means one exact revision entered intake.
- **Under review** means evidence is being checked. It is not approval.
- **Changes requested** means the same revision is not ready. A source change creates a new target.
- **Accepted** means the exact review target passed the published review policy.
- **Deployed** means the recorded contracts exist and their code and source bindings were verified.
- **Activated** means the exact version may be selected for new launches.
- **Available** means the public product surface can prepare a launch for that active version.

## Version boundary

Acceptance never follows a moving branch. It binds one repository, commit, tree, artifact set, fee policy, payout identity, factory, launch profile, dependency set, and parameter envelope.

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

## Suspension and retirement

Programmable may stop new launches for a version when current evidence no longer supports it. This does not rewrite or disable contracts and pools that already exist.

A retired version remains part of the historical record but cannot be selected for a new launch.
