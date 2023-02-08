---
CIP: Unassigned
Title: Protocol Contribution Policy
Discussions: https://www.comp.xyz/t/cip-xx-protocol-contribution-policy
Status: Draft
Type: Meta Process
Author: Jared Bass (jbass-oz), Michael Lewellen (@cylon)
Contributors: 
Created: 2023-1-19
---

## Abstract

This CIP describes process improvements to facilitate the development and evaluation of protocol contributions that ensures community feedback and quality assurance measures are achieved before adoption. This proposal defines a set of steps that each contribution should satisfy, organized into five phases, which capture the lifecycle of a contribution from ideation to final review before being submitted as an on-chain governance proposal.

## Motivation

The purpose of this proposal is to bring clarity to the process of contributing to the Compound protocol. The proposed details describe a very generalized approach that can be applied to most contributions. The described process intends to facilitate contributions by new contributors with minimal burden on continuing contributors. This proposal attempts to minimize prescribing the use of specific tools while maximizing traceability, transparency, and accessibility of evaluation criteria for the Compound community by offering multiple stages where feedback can be provided early and quality assurance steps satisfied.

## Proposal Details

A 5-phase process from idea to adoption to iteratively refine proposals.

![alt text](../assets/cip-2/5-phases.png)

Each phase may have multiple iterations of code refinements and opportunities to incorporate feedback. Efforts are organized into these phases to prepare contributions for review by each audience. Communication is encouraged throughout the phases.

## Idea Review

The goal of the first phase is to share an idea and incorporate community feedback. If applying for a grant, the refined idea should be formalized by the end of the phase and ready to submit.

1.  Provide enough detail to start a discussion as a post in the Compound Forum.
2.  Determine the level of interest of the community before investing effort in a contribution.
3.  Refine the idea and incorporate feedback from the community.
4.  Determine scope and high-level technical details around the solution.
5.  Optional: Draft a CIP-style proposal to receive additional feedback from CIP Editors. A CIP may not be necessary for every contribution but could be useful for soliciting community input in a formal manner, especially for contributions that require complex design decisions.

## Development Review

The goal of the second phase is to deliver feature-complete code with community developer feedback incorporated. This phase is appropriate for contributions that require new contracts or updates to existing contracts.

1.  Develop a draft of the contribution, complete with tests, to submit to community developers for review.
2.  Announce the proposal in the Compound Forum, and optionally the #development Discord channel, with a detailed description of the contribution, expected behavior, and location of repository to solicit feedback. Use the keyword: “CIP-X: Development Review” in your forum post to indicate the status of your contribution.
3.  If contract code is involved, request to be scheduled for an external audit.

## Community Review

The goal of the third phase is to finalize configuration and parameter values with community feedback incorporated.

1.  Submit a pull request and continue to add commits as needed.
2.  Post revised contribution details, complete with testing and simulation results, to the Compound Forum for review. Use the keyword: “CIP-X: Community Review” in your forum post to indicate the status of your contribution.
3.  If contract code is involved, provide a repository location and expected code freeze date to request a final estimate for an external audit.
4.  Generate reports of testing and simulation results.

## External Review

The goal of the fourth phase is to remedy any audit issues. The contract version to deploy in the final phase should be the contract version audited. The only changes to code in this phase should be to remedy audit issues. Any remediation should be reviewed by the auditor.

1.  Submit the pull request and source control commit ID url of the latest contract version to the auditor.
2.  Share latest testing and simulation results with audit status to the community on the Compound Forum and Discord. Use the keyword: “CIP-X: External Review” in your forum post to indicate the status of your contribution.
3.  Share audit results and any other security recommendations to the Community on the Compound Forum and Discord.

## Final Review

The final phase proposes the changes on-chain.

1.  Generate reports of testing and simulation results following the audit based on the final code commit. Use the keyword: “CIP-X: Final Review” in your forum post to indicate the status of your contribution.
2.  Generate simulation results of the migration and proposal.
3.  Submit a pull request against the official protocol repository to incorporate changes.
4.  Sign and execute the migration to submit the proposal on-chain.
5.  Share the pull request with commit ID details and test and simulation results in an announcement to the community on the Compound Forum and Discord that the proposal is pending a vote.
6.  Following a successful vote and execution of the proposal, test that the upgrade works as expected and merge the pull request,

## Rationale

This CIP is intended to formalize the process of contributing to the protocol. These phases resemble current best practices for contributions although generalized to apply to as many scenarios as possible.

The necessity of a clear contribution process is supported by the experiences of past protocol upgrades that resulted in security issues. Despite attempts to test for bugs and provide early notice to community members for feedback, these security issues were not caught until too late. By utilizing a 5-step contribution process, there are now multiple opportunities for quality assurance measures to be verified and for security issues to be caught early.

This process also provides contributors a formal path to completion that does not require them to make decisions about how and when to communicate their development progress and quality assurance efforts to the community. Given the decentralized nature of Compound development and governance, it’s all the more important that contribution expectations be clearly communicated to both contributors and DAO voters.

## Expected Impact

Adopting the proposal is expected to:

* Facilitate contribution by new contributors with minimal burden on continuing contributors.
* Expedite Compound Governor proposal evaluation with early and regular communication of evaluation criteria.
* Increase participation in contributions and evaluation,
* Improve predictability of process duration especially for grant proposals.
* Bolster confidence of protocol changes with transparency and accessibility.
* Provide improved guidance for grant recipients to achieve milestones for payment in the Compound grants program.

## Security Considerations

By formalizing contribution policies for on-chain upgrades and deployments, a higher level of quality assurance can be achieved for each contribution and therefore improve overall protocol security. While this CIP does not describe specific tools to achieve each requirement, we expect that many of the existing testing and security tooling in Compound repositories will be utilized. Additional testing and security tooling may also be developed for Compound repositories to further align and automate this contribution process.

# Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
