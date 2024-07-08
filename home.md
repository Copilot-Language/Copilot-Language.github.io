## News
**Release 3.20 -- 2024-07-07**

We are pleased to announce the release of Copilot 3.20, a stream-based DSL
for writing and monitoring embedded C programs, with an emphasis on correctness
and hard realtime requirements. Copilot is typically used as a high-level
runtime verification framework, and supports temporal logic (LTL, PTLTL and
MTL), clocks and voting algorithms.

Among others, Copilot is being used at the Safety Critical Avionics Systems
Branch of NASA Langley Research Center for monitoring test flights of drones.

This release introduces support to upload the values of fields in structs, and
add support for GHC 9.8. We also remove deprecated functions from
`copilot-language` that had been renamed in prior versions for compatibility
with newer versions of GHC.

Details are available
[here](https://github.com/Copilot-Language/copilot/milestone/27?closed=1),
and
[here](https://github.com/Copilot-Language/copilot/releases/tag/v3.20).

Current emphasis is on introducing support to update the values of elements in
arrays, improving the codebase in test coverage, removing unnecessary
dependencies, hiding internal definitions, and formatting the code to meet our
new coding standards. We also plan to add extensions to be able to visualize
streams. Users are encouraged to participate by opening issues and asking
questions via our [github repo](https://github.com/copilot-language/copilot).

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
