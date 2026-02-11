# awesome-LAFS [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

A curated list of things related to Tahoe-LAFS and its wider ecosystem.
See the [Awesome Lists GitHub topic](https://github.com/topics/awesome-list) for more such lists on many different subjects.

*Contributions welcome!*


## Capability-based Security

  * [Zooko's triangle](https://en.wikipedia.org/wiki/Zooko%27s_triangle) is a trilemma of three properties that some people consider desirable for names of participants in a network protocol: global, secure, and memorable. Zooko conjectured that no single kind of name can achieve more than two.
  * [Good Practices for Capability URLs](https://w3ctag.github.io/capability-urls/) by the W3C TAG (Technical Architecture Group) gives an introduction, examples, potential issues and recommendations when handling capability URLs.  It includes a [short chapter on Tahoe-LAFS](https://w3ctag.github.io/capability-urls/#tahoe-lafs).
  * [Christine Lemmer-Webber, 2018: Petnames: A humane approach to secure, decentralized naming](https://files.spritely.institute/papers/petnames.pdf) Petname systems try to fulfil all three desirable properties.
  * [Marc Stiegler, 2005: An Introduction to Petname Systems](http://www.skyhunter.com/marcs/petnames/IntroPetNames.html)
  * [ERights.org](http://www.erights.org/) E is an object-capability programming language and platform for writing distributed, secure, and robust software.
    * [Lecture: Mark S. Miller, Immunity from Viruses, Safety from Geeks Bearing Gifts (May 9, 2002)](https://www.youtube.com/watch?v=KoM_aCuFk1w)
  * [Miller, Yee, Shapiro 2003: Capability Myths Demolished](https://srl.cs.jhu.edu/pubs/SRL2003-02.pdf)
  * [Mark Samuel Miller: Robust Composition: Towards a Unified Approach to Access Control and Concurrency Control](http://erights.org/talks/thesis/markm-thesis.pdf)
  * [Wikipedia: The Object-capability model](https://en.wikipedia.org/wiki/Object-capability_model)
  * [Wikipedia: The Principle of Least Authority (PoLA)](https://en.wikipedia.org/wiki/Principle_of_least_privilege)
  * [UCAN](https://github.com/ucan-wg/) (User Controlled Authorization Network) is a trustless, secure, local-first, user-originated authorization and revocation scheme.

### Implementations

  * [Cap’n Proto](https://capnproto.org/rpc.html) Data interchange format with a capablity-based RPC protocol.

  * [Capsicum](https://www.cl.cam.ac.uk/research/security/capsicum/) Practical capabilities for UNIX.
    * [Capsicum in FreeBSD](https://wiki.freebsd.org/Capsicum) is part of FreeBSD's main branch.
    * [Talk@BSDCan2014: Andrea Ross: Capsicum and Casper - more than a lipstick on a pig](https://www.youtube.com/watch?v=0la06FHbdvg)

  * [CHERI](https://www.cl.cam.ac.uk/research/security/ctsrd/cheri/) (Capability Hardware Enhanced RISC Instructions) extends conventional processor Instruction-Set Architectures (ISAs) with architectural capabilities to enable fine-grained memory protection and highly scalable software compartmentalization.

  * [Fil-C](https://fil-c.org/) is "a memory safe implementation of the C and C++ programming languages you already know and love".  It uses [InvisiCaps](https://fil-c.org/invisicaps), a capability system for pointers.

  * [Fuchsia](https://fuchsia.dev/) is Google's capability-based "modern open source operating system that's simple, secure, updatable, and performant" ([Wikipedia on Fuchsia](https://en.wikipedia.org/wiki/Fuchsia_(operating_system))).
  * [Redox](https://www.redox-os.org/) Unix-like general-purpose microkernel-based operating system written in Rust.  Its namespaces functionality is inspired by Capsicum.

  * [WASI](https://wasi.dev/) The WebAssembly System Interface (WASI) is an ABI for [Web Assembly (WASM)](https://www.w3.org/TR/wasm-core-2/).
    * [Lin Clark: WASI: A system interface to run WebAssembly outside the web](https://hacks.mozilla.org/2019/03/standardizing-wasi-a-webassembly-system-interface/) Employing capability-based security for robust sandboxing.
    * [Talk: Ed Schouten, 32C3 (2015): CloudABI - Pure capability-based security for UNIX](https://media.ccc.de/v/32c3-7231-cloudabi) CloudABI is a predecessor of WASI.

## Forward Error Correction (FEC) / Erasure Coding

  * [ZFEC on GitHub](https://github.com/tahoe-lafs/zfec/) efficient, portable erasure coding tool
  * [ZFEX on GitHub](https://github.com/WojciechMigda/zfex/) a fork to utilize SIMD instructions ([benchmarks](https://github.com/WojciechMigda/zfex/blob/main/bench/Results.rst))
  * [FECpp](https://www.randombit.net/code/fecpp/) and accompanying [blog post](https://randombit.net/bitbashing/posts/forward_error_correction_using_simd.html) introduce using SSE2 to optimize the GF(2⁸) multiplications and implements a bitwise-compatible algorithm to zfex.

## (Client-Side) Encryption

  * ...

## Secure network transfer

  * [Twisted](https://twisted.org/) An event-driven networking engine.  Tahoe-LAFS relies heavily on Twisted.
  * [Magic Wormhole](https://github.com/magic-wormhole/magic-wormhole) transfers data and files securely between two computers.
  * [FOWL](https://github.com/meejah/fowl) Get TCP streams from one computer to another, safely.
  * [iroh](https://iroh.computer/) Iroh is a library for building on direct connections between devices.

## Distributed Storage

  * [Tahoe-LAFS](https://www.tahoe-lafs.org/)
  * [Sia](https://sia.tech/)
  * [IPFS](https://ipfs.tech/) "store NFTs" 😹

## Tools that work with Tahoe-LAFS

  * [Magic Folder](https://github.com/tahoe-lafs/magic-folder) syncs local folders to a Tahoe-LAFS grid.
    * The [Magic Folder Data Model](https://magic-folder.readthedocs.io/en/latest/datamodel.html) allows multiple writers.
  * [Rclone](https://rclone.org/) syncs and mounts [over 70 cloud storage protocols](https://rclone.org/#providers). (Tahoe-LAFS support via its [SFTP frontend](https://tahoe-lafs.org/trac/tahoe-lafs/wiki/SftpFrontend))
