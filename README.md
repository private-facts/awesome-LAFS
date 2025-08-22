# awesome-LAFS [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

A curated list of things related to Tahoe-LAFS and its wider ecosystem.  
See the [Awesome Lists GitHub topic](https://github.com/topics/awesome) for more such lists on many different subjects. 

*Contributions welcome!*


## Distributed Storage

  * [Tahoe-LAFS](https://www.tahoe-lafs.org/)
  * [Sia](https://sia.tech/)
  * [IPFS](https://ipfs.tech/) "store NFTs" 😹

## Capability-based Security

  * [Good Practices for Capability URLs](https://w3ctag.github.io/capability-urls/) by the W3C TAG (Technical Architecture Group) give an introduction, examples, potential issues and recommendations when handling capability URLs.
    * [Short chapter on Tahoe-LAFS](https://w3ctag.github.io/capability-urls/#tahoe-lafs)
    
## Forward Error Correction (FEC) / Erasure Coding

  * [ZFEC on GitHub](https://github.com/tahoe-lafs/zfec/) efficient, portable erasure coding tool
  * [ZFEX on GitHub](https://github.com/WojciechMigda/zfex/) a fork to utilize SIMD instructions ([benchmarks](https://github.com/WojciechMigda/zfex/blob/main/bench/Results.rst))
  * [FECpp](https://www.randombit.net/code/fecpp/) and accompanying [blog post](https://randombit.net/bitbashing/posts/forward_error_correction_using_simd.html) introduce using SSE2 to optimize the GF(2⁸) multiplications and implements a bitwise-compatible algorithm to zfex.
    
## (Client-Side) Encryption

  * ...

## Secure network transfer

  * [Twisted](https://twisted.org/) An event-driven networking engine.  Tahoe-LAFS relies heavily on Twisted.

## Tools that work with Tahoe-LAFS

  * [Magic Folder](https://github.com/tahoe-lafs/magic-folder) syncs local folders to a Tahoe-LAFS grid.
    * The [Magic Folder Data Model](https://magic-folder.readthedocs.io/en/latest/datamodel.html) allows multiple writers.
  * [Rclone](https://rclone.org/) syncs and mounts [over 70 cloud storage protocols](https://rclone.org/#providers).
