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
  - 
- **`Informational`** An informational UIP describes an Ultrain OS design issue.
- **`Meta`** A meta UIP describes a process surrounding Ultrain OS or proposes a change to(or an event in) a process.

# UIP Work Flow




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
EIPs may include auxiliary files such as diagrams. Such files must be named EIP-XXXX-Y.ext, where “XXXX” is the EIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).


# Transferring EIP Ownership
--
It occasionally becomes necessary to transfer ownership of EIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred EIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the EIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the EIP. We try to build consensus around an EIP, but if that's not possible, you can always submit a competing EIP.

If you are interested in assuming ownership of an EIP, send a message asking to take over, addressed to both the original author and the EIP editor. If the original author doesn't respond to email in a timely manner, the EIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

# UIP Editors

The Current UIP editors are

# EIP Editor Responsibilities
--
For each new EIP that comes in, an editor does the following:

Read the EIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
The title should accurately describe the content.
Check the EIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style
If the EIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the EIP is ready for the repository, the EIP editor will:

Assign an EIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this EIP)

Merge the corresponding pull request

Send a message back to the EIP author with the next step.

Many EIPs are written and maintained by developers with write access to the Ethereum codebase. The EIP editors monitor EIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on EIPs. We merely do the administrative & editorial part.



# Index
- `UIP` Ultrain Improvement Proposal
- `RFC` Request For Comment
- `IETF` Internet Engineering Task Force
- `ISO` International Organization for Standardization