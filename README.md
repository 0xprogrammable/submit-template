<p align="center">
  <a href="https://programmable.market">
    <img src="https://raw.githubusercontent.com/0xprogrammable/0xprogrammable/main/assets/profile/programmable-profile-ecosystem.jpg" alt="Programmable projects connected across a shared ecosystem" width="100%">
  </a>
</p>

<h1 align="center">Submit a Template</h1>

<p align="center">
  Publish a reusable hook template that other people can launch on Programmable.
</p>

> [!IMPORTANT]
> **Status: planned.** Template submissions and public template fee-share activation are not open yet.

<p align="center">
  <a href="#what-belongs-here"><strong>Read what belongs here</strong></a>
  &nbsp;·&nbsp;
  <a href="docs/requirements.md">Read the requirements</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/0xprogrammable/hookbuilder">Build with Hookbuilder</a>
</p>

## What belongs here

A reusable launch template is one versioned product that other creators can configure and launch. It may include a hook, factory, application, or companion service, but every required component and configurable boundary must be reviewed together.

| You want to | Use |
| --- | --- |
| Launch your own token or hook project | [Submit a Launch](https://github.com/0xprogrammable/submit-launch) |
| Publish a reusable template for other creators | This repository |
| Build or test a Uniswap v4 hook | [Hookbuilder](https://github.com/0xprogrammable/hookbuilder) |
| Integrate Programmable launches | [Developer documentation](https://developers.programmable.market) |

## Creator fee

The intended public template policy is **20 bps (0.20%) total** for an activated template version:

| Recipient | Share |
| --- | ---: |
| Template creator | 10 bps (0.10%) |
| Programmable | 10 bps (0.10%) |

This policy is planned and is not active until the template contracts, payout address, fee basis, fee policy, and exact version are verified and activated. This is the total fee under the planned public template policy, not 20 bps plus another 10 bps. Any separate pool or route fee must be disclosed independently. Revenue depends on actual use. Acceptance does not guarantee launches, trading volume, or income.

Partnership templates use a separate policy and review path. They are not submitted through the public template process.

Read [Fees and payouts](docs/fees-and-payouts.md) for the complete boundary.

## What you will submit

An application must identify one exact, public version of the template:

1. Public source repository, numeric repository ID, commit, and tree.
2. Reproducible build instructions and pinned dependencies.
3. Exact contracts, factories, runtime code hashes, and supported chain.
4. Allowed creator inputs and hard parameter limits.
5. Fee policy, payout address, custody, privileged roles, and upgrade controls.
6. Tests, invariants, threat model, and candidate rehearsal evidence.
7. License and confirmation that you may submit the source.

The complete checklist is in [Template requirements](docs/requirements.md).

## How review works

1. Build and test the template in its own public repository.
2. Freeze one exact source revision.
3. Prepare the template application when intake opens.
4. Automated checks validate the package and its source bindings.
5. Review covers behavior, permissions, value flows, parameter limits, fees, and launch compatibility.
6. If accepted, deployment, verification, activation, and availability remain separate later states.
7. Every launch performs its own currentness and parameter checks.

A source, dependency, factory, fee, authority, or parameter-boundary change creates a new template version and a new review target.

Read [Review and activation](docs/review-and-activation.md).

## What acceptance means

Acceptance applies only to the exact version and parameter limits recorded by Programmable. It is not an audit, safety guarantee, endorsement, promise of availability, or promise of earnings. Deployment, activation, currentness, and each user launch remain separate facts.

## Related repositories

- [Hookbuilder](https://github.com/0xprogrammable/hookbuilder) helps a coding agent build and prepare a hook project.
- [Submit a Launch](https://github.com/0xprogrammable/submit-launch) is for one project that you want to launch yourself.
- [Programmable](https://github.com/0xprogrammable/programmable) contains the platform contracts and website.
- [Developers](https://github.com/0xprogrammable/developers) defines the public integration contract.

## Security

Never include private keys, seed phrases, credentials, private RPC URLs, personal data, or unpublished vulnerabilities in a pull request or issue. Read [SECURITY.md](SECURITY.md) before reporting a security problem.

Released under the [MIT License](LICENSE).
