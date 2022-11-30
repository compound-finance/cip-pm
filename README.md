# Compound Improvement Proposal Management Repository

This repository is used for project management for various initiatives affecting the Compound protocol in the form of CIPs (Compound Improvement Proposals). 

Topics tracked in the repo are reviewed on biweekly basis in the Compound Developer Community Calls in [Discord](https://compound.finance/discord).

## CIP Purpose

Compound Improvement Proposals (CIPs) ared used as a default mechanism to propose standards, processes and enhancements intended to improve the Compound Protocol  as both on-chain code changes and off-chain processes. See [CIP-1: Purpose and Guidelines]() for more information.

## Directory Structure

- [`finalized`](./finalized) - contains CIPs that have been approved and finalized
- [`drafts`](./drafts) - contains CIP drafts that are not yet approved
- [`CIP-TEMPLATE.md`](./drafts/CIP-TEMPLATE.md) - template CIP to be used for new CIP drafts
- [assets](./assets) - used to store assets for CIPs such as images

## CIP Contribution Guide

#### Creating a CIP

CIPs can start out as ideas for improving Compound that any community member can propose. If a CIP Author wishes to get feedback on a particular idea or known issue, they can submit an issue in this repo for feedback and/or discuss the idea in the [Compound Community Forum](https://www.comp.xyz/).

CIPs should be drafted using the [following template]() which may be forked against this repository. The Draft should include content for all sections in the template that are not marked _optional_ and be written as a [GitHub-flavored Markdown](https://github.github.com/gfm/) document added to the cip-drafts directory. It should then be submitted as a Pull Request against the repostitory.

### Approving a CIP

Once submitted as a Pull Request, a CIP will be assigned a CIP Editor for Review. This Editor will ensure the CIP meets the formatting requirements and also suggest any areas of improvement they see. Once a CIP Editor has confirmed that a CIP meets the minimuim requirements, it will be assigned a number and submitted as an agenda item in the next community call. 

In the Community Call, the CIP will be presented by the author or someone else nominated by them to present it. They will answer questions from other CIP Editors and Community Members. If any objections or areas of improvement are raised by CIP Editors, the CIP Author will be asked to address the feedback and present again in the next community call. At this point, an CIP may be approved with no objections or a majority support of CIP Editors at which point it will move into a Final Call status for two weeks before moving to implementation.

### Implementing a CIP

TODO




