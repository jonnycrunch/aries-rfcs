# Aries RFC

This repo holds RFCs for the Aries project. They describe important
topics ([not minor details](#do-you-need-an-RFC) that we want to
standardize across the Aries ecosystem. There are 2 types of RFCs:

* RFCs that describe individual features (the [/features](./features) folder)
* RFCs that explain concepts underpinning many features (the [/concepts](./concepts) folder)

RFCs are for developers *building on* Aries. They don't provide guidance on how Aries implements features internally; individual Aries repos have design docs for that.

### RFC Lifecycle

RFCs go through a standard lifecycle:

![lifecycle](lifecycle.png)

* To __propose__ an RFC, [raise a PR](#how-to-propose-an-RFC) against this repo. Proposed RFCs are considered a Work in Progress.
Status => PROPOSED

* To get an RFC __accepted__ or merged, [build consensus](#how-to-get-an-RFC-accepted)
  for your RFC on [Rocket Chat](http://chat.hyperledger.org/#aries) and in community meetings. RFCs are merged as soon as the community thinks they reasonably embody an idea worth standardizing. A merged RFC is incubating on a standards track. Status => ACCEPTED

* To get an RFC __adopted__, [socialize and implement](#how-to-get-a-hipe-adopted).
Once a RFC has momentum, it is formally given the "adopted" status. This happens
when implementations accumulate, or when the mental model it advocates has begun
to permeate our discourse. In other words, adoption is acknowledgment of a _de facto_
standard. Status => ADOPTED

* To __refine__ an RFC, propose changes to it through additional PRs. Typically
  these changes are driven by experience that accumulates during or after adoption.
  Minor refinements that just improve clarity can happen inline with lightweight
  review. Status is still ADOPTED

    Significant refinements require a superseding document; the original RFC is
    __superseded__ with a forwarding hyperlink, not replaced. Status => SUPERSEDED

### Do you need an RFC?

Use a RFC to advocate substantial changes to the Aries ecosystem, where
those changes need to be understood by developers who use Aries.

### How to propose an RFC

Before writing a RFC, consider exploring the idea on [Rocket Chat](
http://chat.hyperledger.org/#aries), on community calls (see the 
[Hyperledger Community Calendar](
https://wiki.hyperledger.org/community/calendar-public-meetings)),
or on [aries@lists.hyperledger.org](
mailto:aries@lists.hyperledger.org). Encouraging feedback from maintainers
is a good sign that you're on the right track.

#### Mechanics

  - Fork [the RFC repo](https://github.com/hyperledger/aries-RFC).
  - Pick a folder name for your RFC. The name should consist of a zero-padded
    4-digit number plus a descriptive name for the topic. Use lower-kebab-case
    for the descriptive name. Get the RFC number by finding the number
    of [the most recent pull request](https://github.com/hyperledger/aries-rfc/pulls)
    and incrementing by 1. For example, if the highest numbered PR is 125, your
    RFC number would be 126. You should end up with a folder name like
    `0026-my-cool-feature`.
  - Create the folder and copy `0000-template.md` to `text/<your folder name>/README.md`.
  - Fill in the RFC. Put care into the details: RFCs that do not present
    convincing motivation, demonstrate an understanding of the impact of the
    design, or are disingenuous about the drawbacks or alternatives tend to be
    poorly received. You can add supporting artifacts, such as diagrams and sample
    data, in the RFC's folder.
  - Submit a pull request.

Make sure that all of your commits satisfy the [DCO requirements](
https://github.com/probot/dco#how-it-works) of the repo.

The RFC Maintainers will check to see if the process has been followed, and request any process changes before merging the PR. 

When the PR is merged, your RFC is now in the PROPOSED state.

### How to get an RFC accepted

After your RFC has been proposed, the RFC will receive feedback from the larger
community, and the author should be prepared to revise it. Updates may be made via pull request, and those changes will be merged as long as the process is followed.

When you believe that the RFC is mature enough (feedback is somewhat resolved,
consensus is emerging, and implementation against it makes sense), submit a PR that changes the Status to ACCEPTED. The status change PR will remain open until the maintainers agree on the status change.

>NOTE: contributors who used the Indy HIPE process prior to May 2019 should
see the acceptance process substantially simplified under this approach.
The bar for acceptance is not perfect consensus and all issues resolved;
it's just general agreement that a doc is "close enough" that it makes
sense to put it on a standards track where it can be improved as
implementation teaches us what to tweak.

### How to get an RFC adopted

An accepted RFC is a standards-track document. It becomes an acknowledged
standard when there is evidence that the community is deriving meaningful
value from it. So:

- Implement the ideas, and find out who else is implementing.
- Socialize the ideas. Use them in other RFCs and documentation.
- Update the agent test suite to reflect the ideas.

When you believe an RFC is a _de facto_ standard, raise a PR that changes the status to ADOPTED.  If the community is friendly to the idea, the doc
will enter a two-week "Final Comment Period" (FCP), after which there will
be a vote on disposition.

## About

#### License

This repository is licensed under an [Apache 2 License](LICENSE).

#### Contributions

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the repo by you, as defined in the Apache-2.0 license, shall be
licensed as above, without any additional terms or conditions.

#### Acknowledgement

The structure and a lot of the initial language of this repository was borrowed from [Indy HIPEs](<https://github.com/hyperledger/indy-hipe>), which borrowed it from [Rust RFC](https://github.com/rust-lang/rfcs).
Their good work has made the setup of this repository much quicker and better than it otherwise would have been.
If you are not familiar with the Rust community, you should check them out.