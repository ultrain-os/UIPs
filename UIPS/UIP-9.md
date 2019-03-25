UIP | title | status | type | author | created
----|---|---|---|---|---|---|---
1| UIP Purpose and Guidelines| Active| Meta| Ultrain core team | 2019-01-30

# What is an UIP?
--

UIP is short for `Ultrain-Os Imporvement Proposal`. An UIP document providing information and guidelines to the Ultrain community, or describing a new feature for Ultrain or its processes or environment. The UIP should provide a concise technical specification of the feature and a rationale for the feature. The UIP author is responsible for building consensus within the community and documenting dissenting opinions.

# UIP Rationale
--

We intend UIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into Ultrain. Because the UIPs are maintained as text files in a versioned repository, their revision hisUIPtory is the historical record of the feature proposal.

For UIP implementers, UIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the UIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.


# UIP Types
--
The belows are UIP types:

- **`Standard Track`** A Standard Track UIP describes any change that affects most or all Ultrain OS implements, such as a change to the network protocal, proposed application standards/conventions.
- **`Informational`** An informational UIP describes an Ultrain OS design issue.
- **`Meta`** A meta UIP describes a process surrounding Ultrain OS or proposes a change to(or an event in) a process.

# UIP Work Flow
--

Parties involved in the process are you, the champion or *UIP author*, the [*UIP editors*](#uip-editors)).

:warning: Before you begin, vet your idea, this will save you time. Ask the ultrain community first if an idea is original to avoid wasting time on something that will be be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where Ultrain is used. Examples of appropriate public forums to gauge interest around your UIP include [the Issues section of this repository], and [one of the Ultrain developer website]. In particular, [the Issues section of this repository] is an excellent place to discuss your proposal with the community and start creating more formalized language around your UIP.

Your role as the champion is to write the UIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful UIP will move along:

```
[ WIP ] -> [ DRAFT ] -> [ LAST CALL ] -> [ ACCEPTED ] -> [ FINAL ]
```

Each status change is requested by the UIP author and reviewed by the UIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your UIP. The UIP editors will process these requests as per the conditions below.

* **Active** -- Some Informational and Process UIPs may also have a status of “Active” if they are never meant to be completed. E.g. UIP 1 (this UIP).
* **Work in progress (WIP)** -- Once the champion has asked the Ultrain community whether an idea has any chance of support, they will write a draft UIP as a [pull request]. Consider including an implementation if this will aid people in studying the UIP.
  * :arrow_right: Draft -- If agreeable, UIP editor will assign the UIP a number (generally the issue or PR number related to the UIP) and merge your pull request. The UIP editor will not unreasonably deny an UIP.
  * :x: Draft -- Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not in keeping with the Ultrain philosophy.
* **Draft** -- Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the UIP to be mature and ready to proceed to the next status. An UIP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core UIPs).
  * :arrow_right: Last Call -- If agreeable, the UIP editor will assign Last Call status and set a review end date (`review-period-end`), normally 14 days later.
  * :x: Last Call -- A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that UIPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed.
* **Last Call** -- This UIP will listed prominently on the https://UIPs.ethereum.org/ website (subscribe via RSS at [last-call.xml](/last-call.xml)).
  * :x: -- A Last Call which results in material changes or substantial unaddressed technical complaints will cause the UIP to revert to Draft.
  * :arrow_right: Accepted (Core UIPs only) -- A successful Last Call without material changes or unaddressed technical complaints will become Accepted.
  * :arrow_right: Final (Not core UIPs) -- A successful Last Call without material changes or unaddressed technical complaints will become Final.
* **Accepted (Core UIPs only)** -- This UIP is in the hands of the Ethereum client developers.  Their process for deciding whether to encode it into their clients as part of a hard fork is not part of the UIP process.
  * :arrow_right: Final -- Standards Track Core UIPs must be implemented in at least three viable Ethereum clients before it can be considered Final. When the implementation is complete and adopted by the community, the status will be changed to “Final”.
* **Final** -- This UIP represents the current state-of-the-art. A Final UIP should only be updated to correct errata.

Other exceptional statuses include:

* **Deferred** -- This is for core UIPs that have been put off for a future hard fork.
* **Rejected** -- An UIP that is fundamentally broken or a Core UIP that was rejected by the Core Devs and will not be implemented.
* **Active** -- This is similar to Final, but denotes an UIP which may be updated without changing its UIP number.
* **Superseded** -- An UIP which was previously final but is no longer considered state-of-the-art. Another UIP will be in Final status and reference the Superseded UIP.




# What belongs in a successful UIP?
--
Each UIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the UIP, including the UIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See below for details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the UIP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (*optional) - The motivation is critical for UIPs that want to change the Ethereum protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the UIP solves. UIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current Ethereum platforms (cpp-ethereum, go-ethereum, parity, ethereumJ, ethereumjs-lib, and others.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Backwards Compatibility - All UIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The UIP must explain how the author proposes to deal with these incompatibilities. UIP submissions without a sufficient backwards compatibility treatise may be rejected outright.
- Test Cases - Test cases for an implementation are mandatory for UIPs that are affecting consensus changes. Other UIPs can choose to include links to test cases if applicable.
- Implementations - The implementations must be completed before any UIP is given status “Final”, but it need not be completed before the UIP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.
- Copyright Waiver - All UIPs must be in the public domain. See the bottom of this UIP for an example copyright waiver.





# UIP Formats and Templates
UIPs should be written in [markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax/) format. Image files should be included in a subdirectory of the `assets` folded for that UIP as follow: `assets/uip-X`(for uip X). When linking to an image in the UIP, use relative links such as `../asserts/UIP-X/image.png`.

# UIP Header Preamble
The UIP must begin with an [RFC 822](https://tools.ietf.org/html/rfc822) style header preamble. The headers must appear in the following order. Headers marked with `*` are optional and are described below. All other headers are required.

`UIP:`\<UIP number> (this is determined by the UIP editor)

`title:`

`author:` \<a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.>

`*discussions-to:` < a URL pointing to the official discussion thread >

`status:` <Draft | Last Call | Accepted | Final | Active | Deferred | Rejected | Superseded>

`* review-period-end:`

`type:`\<Standards Track | Informational | Meta>

`created:`

`* requires:`\<UIP number(s)>

`* replaces`:\<UIP number(s)>

`* superseded-by:`\<UIP number(s)>

`* resolution:`\<a URL pointing to the resolution of this UIP>

Headers that permit lists must separate elements with commas.

Headers requiring dates will alyws do so in the format of ISO 8610(yyyy-mm--dd)

# Auxiliary Files
--
UIPs may include auxiliary files such as diagrams. Such files must be named UIP-XXXX-Y.ext, where “XXXX” is the UIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).


# Transferring UIP Ownership
--
It occasionally becomes necessary to transfer ownership of UIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred UIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the UIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the UIP. We try to build consensus around an UIP, but if that's not possible, you can always submit a competing UIP.

If you are interested in assuming ownership of an UIP, send a message asking to take over, addressed to both the original author and the UIP editor. If the original author doesn't respond to email in a timely manner, the UIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

# UIP Editors
--
The Current UIP editors are




# UIP Editor Responsibilities
--
For each new UIP that comes in, an editor does the following:

Read the UIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
The title should accurately describe the content.
Check the UIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style
If the UIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the UIP is ready for the repository, the UIP editor will:

Assign an UIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this UIP)

Merge the corresponding pull request

Send a message back to the UIP author with the next step.

Many UIPs are written and maintained by developers with write access to the Ethereum codebase. The UIP editors monitor UIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on UIPs. We merely do the administrative & editorial part.



### Bibliography


# Index
- `UIP` Ultrain Improvement Proposal
- `RFC` Request For Comment
- `IETF` Internet Engineering Task Force
- `ISO` International Organization for Standardization