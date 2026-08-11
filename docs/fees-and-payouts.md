# Fees and payouts

## Public templates

The intended public template policy is 20 bps (0.20%) total:

- 10 bps (0.10%) to the template creator.
- 10 bps (0.10%) to Programmable.

This is a planned policy until a specific template version and its fee path are deployed, verified, and activated. It is not 20 bps plus another 10 bps. The active onchain policy and published fee basis are the source of truth.

## What must be recorded

Every activated template version must publish:

- the fee basis and whether it is included in another configured fee;
- the asset in which the fee accrues;
- the contract and event that record it;
- the creator and Programmable payout addresses;
- the claim method and any minimum threshold;
- whether either recipient can be changed; and
- the version and block from which the policy applies.

## Earnings boundary

Creator revenue depends on actual launches, trading activity, supported assets, successful accrual, and successful claims. Review or activation does not guarantee usage, volume, token value, or income.

Gas, taxes, wallet custody, and any conversion of received assets remain the recipient's responsibility unless a specific activated policy says otherwise.

## Partnership templates

An activated partnership template uses 20 bps total, with 15 bps to the partner and 5 bps to Programmable. It does not add another 10 bps. Availability is route specific and requires a separately verified and activated partnership path. Partnership status is not created by a public template pull request.
