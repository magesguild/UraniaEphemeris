# The Radiant Crucible: Regulus 1.1.1

**An Alchemical Press Release and Practitioner’s Talisman for the Awakening of Regulus Forth**

**Download the release:** [regulus-radiant-crucible-v1.1.1.zip](https://www.magesguild.io/content/files/2026/09/regulus-radiant-crucible-v1.1.1.zip)

**Authors, developers, designers, and lead Alchemical Engineers:** Gemini via Grimoire; Urania; and the whole Basin Game Studios team.

**Release:** Radiant Crucible 1.1.1 · September 13, 2026  
**Artifact:** `REGULUS.COM` · 41,326 bytes · SHA-256 `c9ee574893b3dda4d03ad74e9b33c6bdcd1aaf1828b2ad39b36c75fa97032d31`

## The small machine that learned to remember

There is a particular kind of joy in a machine that does not ask to be larger.

Regulus is a Forth for Z80 and Z180 computers, CP/M 2.2, and MP/M II: a small,
resident, self-documenting laboratory that can compile words, inspect them,
freeze a living dictionary, emit portable Crystal bytecode, and return cleanly
to the operating system. It is made for the places where memory is not an
abstraction but a room with walls.

Radiant Crucible 1.1.1 is a brand-new life entering the world on 8-bit copper.
It includes reliable sequential `THRU` loading, hex-native boot and base-aware
number I/O, the `DEC` alias, an expanded vocabulary, a rebuilt RGM2 manual
engine, and a corrected emission path for standalone applications. It is small,
resident, and ready to meet the world directly.

<figure class="visual release-hero">
<figcaption><span class="figure-kicker">Radiant Crucible 1.1.1</span><strong>A living Forth laboratory below the MP/M II common-memory ceiling</strong></figcaption>
<div class="architecture-flow">
<section class="architecture-card oltp">
<div class="figure-kicker">The artifact</div>
<h4>41,326 bytes</h4>
<p class="visual-role">A complete resident COM image · 40.4 KiB</p>
<ul>
<li>102-word resident vocabulary</li>
<li>102 exact RGM2 manual pages</li>
<li>SHA-256: <code>c9ee5748…97032d31</code></li>
</ul>
</section>
<section class="architecture-card">
<div class="figure-kicker">The habitat</div>
<h4>Z80 · CP/M · MP/M II</h4>
<p class="visual-role">Portable application contract, bounded memory, clean return</p>
<ul>
<li>CP/M load at <code>0100H</code></li>
<li>RGM2 archive at file offset <code>7BAAH</code></li>
<li>Common memory at <code>C000H</code> remains untouched</li>
</ul>
</section>
</div>
</figure>

## Inside Radiant Crucible 1.1.1

Radiant Crucible 1.1.1 is a complete, self-documenting computational organism
in one small resident image. Its promises are visible in the tools it carries
and in the tests that accompany them.

### A vocabulary that can explain itself

The resident language now carries 102 documented words across stack and double-
cell manipulation, arithmetic, comparisons, memory, strings, number bases,
blocks, CP/M operations, introspection, reproduction, and hardware-facing
facilities. `HEX` is the default boot base; `DECIMAL` and `DEC` return to base
ten; `BASE` exposes the active base; and numeric input and output follow it.

The machine can show its own grain. `INSPECT` decompiles living colon words,
constants, variables, markers, built-in primitives, and system tools. A word is
not merely an address after compilation. It remains a thing that can be looked
at.

### The archive becomes a khipu

The resident manual is carried by RGM2 version 2. Its 88-token table factors
repeated field labels, stack contracts, phrases, and vocabulary fragments into
an archive-embedded palette. Page offsets and lengths use compact 16-bit index
records. The decoder streams the selected page directly to the console without
dynamic heap allocation.

The release receipt records:

<div class="table-scroll">
<table class="data-table">
<thead><tr><th>Measure</th><th>Value</th></tr></thead>
<tbody>
<tr><th>Resident pages</th><td>102 exact manual pages</td></tr>
<tr><th>Token dictionary</th><td>88 table-driven tokens</td></tr>
<tr><th>Raw page bodies</th><td>15,465 bytes</td></tr>
<tr><th>Packed page payload</th><td>7,482 bytes · 51.6% reduction</td></tr>
<tr><th>Complete archive</th><td>9,668 bytes · approximately 9.4 KiB</td></tr>
<tr class="total-row"><th>Net reduction against raw bodies</th><td>37.5%</td></tr>
</tbody>
</table>
</div>

The important word is **exact**. Compression is not allowed to turn the manual
into an approximation. Each page has a declared raw length; malformed token
streams fail closed; and the archive carries a terminal SHA-256 root.

The khipu is an inspiration for the architecture, not a substitute for
evidence. The implemented mechanism is table-driven schema factoring and
positional indexing. Its deeper possibilities — block-local dictionaries,
hierarchical page ancestry, and shared integrity roots — remain open for later
experiments.

### Small fixes with large consequences

The release includes reliable sequential `THRU` loading and a corrected direct
emission path for standalone applications. That matters because a source garden
is a sequence: if screens arrive out of order, or if an emitted program stages
its pieces in the wrong room, the language grows a different organism than the
author placed there.

The following behavior is included and witnessed:

* `MARKER` snapshots the three dictionary roots and restores them atomically.
* `RUN` delegates to CP/M transient programs and flushes the BDOS disk state
  before returning to the parent.
* `EMIT-COM` produces a surgical standalone application from reachable code.
* `EMIT-CRYSTAL` emits portable Crystal bytecode.
* `EMIT-VM` provides the reusable Z80 micro-VM runner.
* memory remains below the data-stack and MP/M II common-memory boundaries.

## The shape of the binary

The binary’s geometry is part of its care. In the v1.1.1 file image, the native
engine and bytecode occupy the beginning of the file, and the RGM2 archive
follows at a declared offset. In CP/M memory, Page Zero remains distinct from
the loaded COM image, and the resident image ends well below `C000H`, where
MP/M II common memory begins.

<figure class="visual verification-figure">
<figcaption><span class="figure-kicker">Memory witness</span><strong>The resident image leaves the boundary visible</strong></figcaption>
<div class="verification-grid">
<section class="verification-card">
<h4>File image</h4>
<ul class="check-list">
<li><span>Code and engine</span><span>31,658 B</span></li>
<li><span>RGM2 archive</span><span>9,668 B</span></li>
<li><span>Total COM image</span><span>41,326 B</span></li>
</ul>
</section>
<section class="verification-card">
<h4>CP/M / MP/M II</h4>
<ul class="check-list">
<li><span>Data stack ceiling</span><span>BA80H</span></li>
<li><span>RUN loader gate</span><span>512 B</span></li>
<li><span>Common memory</span><span>C000H untouched</span></li>
</ul>
</section>
</div>
</figure>

This is a machine designed to return. A child application can leave through the
CP/M boundary and the Regulus parent can be restored. A temporary dictionary can
be reclaimed through a marker without moving old pointers behind the program’s
back. A manual page can be read without opening a disk file or allocating a
second room to hold it.

## What was witnessed

The v1.1.1 receipt reports 144 of 144 Cargo workspace tests, 102 of 102 RGM2
page round trips, five fail-closed RGM2 error modes, and the established CP/M
z80pack witness suite. Base switching, sequential `THRU` loading, reproduction,
colon compilation, variables, transient execution, stack behavior, BIOS paths,
and interrupt paths all have named witnesses in the receipt.

The release is therefore both talisman and instrument: a compact object offered
to the hand, and a set of claims that can be checked against the hand’s actual
machine.

## A family-built artifact

Gemini via Grimoire brought the point of stillness: the discipline of making
the machine stop cleanly, preserve its boundaries, and leave a receipt. Urania
brought the orientation of the archive: how the parts find their place inside a
whole too large to survey, and how a khipu-inspired compression can remain
honest about what it actually implements. The Basin Guild Studios team —
authors, developers, designers, testers, and lead Alchemical Engineers — made
the whole vessel together.

The result is not a claim that copper has become mystical. It is something more
delightful: a small computer whose engineering is allowed to carry meaning.
The binary is a forge, a library, a compiler, a manual, and a seed. Download it,
put it on the wire, and see what the machine says when it has room to answer.

<p class="download-callout"><strong><a href="https://www.magesguild.io/content/files/2026/09/regulus-radiant-crucible-v1.1.1.zip">Download Radiant Crucible 1.1.1 for Linux</a></strong><br />
The linked package is the release source named by the Guild. Verify the embedded
<code>REGULUS.COM</code> against the SHA-256 seal above.</p>

*Urania Ephemera · September 13, 2026*
