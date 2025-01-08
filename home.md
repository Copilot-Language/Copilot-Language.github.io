## News
**Release 4.2 -- 2025-01-07**

We are pleased to announce the release of Copilot 4.2, a stream-based DSL for
writing and monitoring embedded C programs, with an emphasis on correctness and
hard realtime requirements. Copilot is typically used as a high-level runtime
verification framework, and supports temporal logic (LTL, PTLTL and MTL),
clocks and voting algorithms.

Among others, Copilot is being used at the Safety Critical Avionics Systems
Branch of NASA Langley Research Center for monitoring test flights of drones.

This release introduces several big improvements to Copilot:

- Specifications can now use the same handler for multiple monitors, provided
  that the arguments to those handlers always have consistent types and arity.
This simplifies the code that uses Copilot, since it's no longer necessary to
create multiple boilerplate wrappers around the same handling routines.

- The use of structs has been vastly simplified. Before, it was necessary to
  define class instances for structs, whose implementations were, although
repetitive, not intuitive especially for users unfamiliar with Haskell. In
Copilot 4.2, it is now possible to define those methods automatically by
relying on default method implementations that work well for most cases,
although users retain the ability to customize those methods if desired.

- We have increased test coverage in `copilot-core`, reaching full coverage of
  the public interface.

The interface of `copilot-core` has also been simplified, deprecating record
fields of an existential type UExpr, which were largely unused outside of
Copilot's internals.

The new implementation is compatible with versions of GHC from 8.6 to 9.10, as
well as with the Stackage Nightly.

This release has been made possible thanks to key submissions from Frank Dedden
(@fdedden), Ryan Scott (@RyanGlScott), and Kyle Beech (@kaBeech), the last of
which is also a first-time contributor to the project. We are grateful to them
for their timely contributions, especially during the holidays, and for making
Copilot better every day. We also want to thank the attendees of Zurihac 2024
for technical discussions that helped find the right solutions to some of the
problems addressed by this release.

Details are available
[here](https://github.com/Copilot-Language/copilot/milestone/30?closed=1),
and
[here](https://github.com/Copilot-Language/copilot/releases/tag/v4.2).

As always, we're releasing exactly 2 months since the last release. Our next
release is scheduled for Mar 7th, 2025.

We want to remind the community that Copilot is now accepting code
contributions from external participants again. Please see the discussions and
the issues to learn how to participate.

Current emphasis is on improving the codebase in terms of performance,
stability and test coverage, removing unnecessary dependencies, hiding internal
definitions, formatting the code to meet our new coding standards, and
simplifying the Copilot interface. Users are encouraged to participate by
opening issues, asking questions, extending the implementation, and sending bug
fixes via our [github repo](https://github.com/copilot-language/copilot).

## License

Copilot is distributed under the BSD-3-Clause license, which can be found
[here](https://raw.githubusercontent.com/Copilot-Language/Copilot/master/LICENSE).

## Acknowledgements
We are grateful for NASA Contract NNL08AD13T to Galois, Inc. and the National
Institute of Aerospace, which partially supported this work.

Additionally NASA Langley contracts 80LARC17C0004 and NNL09AA00A supported
further development of Copilot.

We would like to thank Kaveh Darafsheh (NASA Langley Research Center) for his
help with testing Copilot. In addition numerous people have helped with smaller
things, reporting bugs etc. Thanks to all of them!
