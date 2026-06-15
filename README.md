# te-re-engineering

> A curated directory of reverse-engineering, custom firmware, tools, mods, and teardowns for Teenage Engineering gear.

Teenage Engineering ships deliberately closed, opinionated hardware. This list maps the community that pries it open - custom firmware, reverse-engineered file formats and protocols, sample and patch tooling, hardware mods, and teardown/recovery notes - device by device.

**Scope:** real, working, TE-specific projects only. Curate, don't collect - see [Contributing](CONTRIBUTING.md).

**Status tags:** an entry is actively maintained unless tagged `(dormant)` (works, but quiet), `(archived)` (read-only), or `(WIP)` (announced, no usable release yet). Half of any niche hardware scene is dormant; we say so rather than hide it.

## Contents

- [SP-1 / Stem Player](#sp-1--stem-player)
- [TP-7](#tp-7)
- [OP-XY](#op-xy)
- [OP-Z](#op-z)
- [OP-1 / OP-1 field](#op-1--op-1-field)
- [EP-133 K.O. II / EP-1320](#ep-133-ko-ii--ep-1320)
- [Pocket Operators](#pocket-operators)
- [Cross-device tools](#cross-device-tools)

## SP-1 / Stem Player

*Small but genuinely active (2024-2026). TE never officially released the SP-1, so everything here is community reverse engineering: a closed forum thread (now archived), a half-dozen GitHub authors, and timknapen/SP-1-dev as the hub.*

### Custom firmware & OS

- [sp1-midi](https://github.com/ericlewis/sp1-midi) - Zephyr BSP/template that is the foundation for building custom SP-1 synths, MIDI controllers, or firmware.
- [sp1-tape-looper](https://github.com/chattock/sp1-tape-looper) - Four-track tape-machine looper firmware that ships a known-good recovery bin.
- [marisko](https://github.com/softmodded/marisko) - Community custom firmware plus a ready-to-use Zephyr board definition for the SP-1.
- [VF-1 Liminal Loop Player OS](https://op-forums.com/t/vf-1-liminal-loop-player-os-for-te-stem-player/31639) - Loop-player OS with per-track mute/solo and master FX, forum-announced but no public download yet. (WIP)

### Reverse engineering & docs

- [SP-1-dev](https://github.com/timknapen/SP-1-dev) - The hub: GPIO pinout, bootloader protocol, eMMC notes, and a dev wiki for writing firmware.
- [SP-1-knowledgebase-skill](https://github.com/dot-Justin/SP-1-knowledgebase-skill) - Cited, curated SP-1 technical reference library packaged as a Claude agent skill.

### Tools & software

- [spire](https://github.com/softmodded/spire) - Renode-based SP-1 emulator that tests firmware with zero brick risk before flashing.
- [sp1-merge](https://github.com/softmodded/sp1-merge) - CLI tool to encode and merge Demucs stems into an SP-1-compatible WAV.
- [Stem Player Studio](https://github.com/humperdink13/TE-StemPlayer) - Desktop app to manage the SP-1, including a host-side Python firmware flasher.
- [solderless.engineering](https://solderless.engineering) - Web updater that loads custom stems and flashes firmware without opening the unit.

### Teardown, flashing & recovery

- [ESP32_nRF52840_glitch](https://github.com/timknapen/ESP32_nRF52840_glitch) - ESP32 tool to read/write internal nRF52 flash over SWD/glitch, used for SP-1 recovery. (dormant)

### Community

- [TE SP-1 lines thread archive](https://github.com/dot-Justin/TE-SP-1-lines-thread-archive) - Public archive of the 846-post reverse-engineering thread, also live at sp-1.dotjust.in.
- [lines TE Stem Player thread](https://llllllll.co/t/te-stem-player/66795) - The primary forum thread, now closed, where SP-1 reverse engineering happened. (archived)

## TP-7

*Thin and locked-down: there is no firmware jailbreak or custom OS for the TP-7 - the OS is closed and updated only through TE's official channel. Real activity is limited to a few companion tools that talk to the device over its supported USB/BLE/MIDI and polyWAV interfaces, plus one teardown effort.*

### Reverse engineering & docs

- [TP-7 guide: going deeper](https://www.spongefile.com/tp-7-guide-going-deeper) - Independent cheat-sheet decoding the TP-7's opaque UI, multitrack, loop and cue workflows.

### Tools & software

- [tp7-midi](https://github.com/lucidyan/tp7-midi) - Web app that documents the TP-7's quirky MIDI CC behavior while driving transport, loops and cues over Web MIDI/BLE.
- [tp7-util](https://github.com/mellson/tp7-util) - macOS app to split and combine TP-7 multitrack polyWAV stems for DAW workflows.
- [TP-7-VoiceSync](https://github.com/armynante/TP-7-VoiceSync) - macOS menu bar app that auto-syncs, transcribes and files TP-7 voice memos to Apple Notes.

### Teardown, flashing & recovery

- [TP-7 Disassembly Tools](https://www.printables.com/model/1478390-teenage-engineering-tp-7-disassembly-tools) - 3D-printable non-standard tools to open a TP-7, though the author warns disassembly likely bricks it. (dormant)

### Community

- [Teenage Engineering TP-7 thread (lines)](https://llllllll.co/t/teenage-engineering-tp-7/63256) - The main community hub for TP-7 workflows, tips and teardown chatter.

## OP-XY

*The newest device (late 2024) and the liveliest of the OP-series scenes, but momentum is concentrated in preset/sample builders and one solid format reverse-engineering effort, not deep firmware hacking.*

### Reverse engineering & docs

- [kmorrill/xy-format](https://gist.github.com/kmorrill/506d69e251f225c0fffb2596c17b9db3) - Community reverse-engineering notes on the OP-XY .xy binary project format, the anchor reference for the scene.

### Tools & software

- [kmorrill/op-xy-vibing](https://github.com/kmorrill/op-xy-vibing) - AI-assisted JSON loop editor that plays to OP-XY over USB-C MIDI and exports presets.
- [buba447/OPXY-Multisample-Tool](https://github.com/buba447/OPXY-Multisample-Tool) - Python scripts to record and pack WAV/AIFF samples into OP-XY multisample presets.
- [buba447 OP-XY Drum & Multisample Patch Generator](https://buba447.github.io/opxy-drum-tool) - Hosted web generator that builds OP-XY drum kits and multisample patches from audio files.
- [sixthlaw/opxy-multisampler-preset-builder](https://github.com/sixthlaw/opxy-multisampler-preset-builder) - Browser tool to drag-drop audio into OP-XY multisampler preset folders with automatic pitch detection.
- [discepoli/op-xy-drum-preset-builder](https://github.com/discepoli/op-xy-drum-preset-builder) - Builds OP-XY drum sampler presets from a list of sample files. (WIP)

## OP-Z

*Mature but slow-moving: the deep reverse-engineering work (libopz, z-po-project) is mostly done, and recent activity is concentrated in videopaks and controller bindings rather than firmware.*

### Reverse engineering & docs

- [libopz](https://github.com/patriciogonzalezvivo/libopz) - Unofficial C++ library to parse .opz project files and talk to the OP-Z over MIDI/SysEx.
- [z-po-project](https://github.com/lrk/z-po-project) - Reverse-engineering wiki documenting OP-Z internals, the closest thing to a protocol bible. (archived)

### Tools & software

- [videolab](https://github.com/teenageengineering/videolab) - Official Unity toolset for building OP-Z videopaks, the foundation every custom videopak is built on.
- [VideolabTest](https://github.com/keijiro/VideolabTest) - Worked videolab shader/effect examples that show how to actually build a videopak. (dormant)
- [OP-Z-Videopak](https://github.com/berndpl/OP-Z-Videopak) - Ready-made collection of OP-Z videopaks to drop in or learn from. (dormant)
- [op-z-m-vave-smk-25](https://github.com/tsoop-com/op-z-m-vave-smk-25) - MIDI bindings that drive the OP-Z sequencer from a cheap M-Vave wireless controller. (dormant)
- [connect-opz](https://github.com/xmacex/connect-opz) - Lua script to wire the OP-Z in as an audio device on the monome norns. (dormant)
- [OPZgo](https://github.com/chrisdiana/OPZgo) - Python utility for ultra-portable OP-Z backups with no computer needed. (dormant)

### Hardware mods

- [OP-Z-Cube](https://github.com/MateSteinforth/OP-Z-Cube) - Arduino-driven LED light object that reacts live to the OP-Z. (dormant)

## OP-1 / OP-1 field

*Healthy but lopsided: the original OP-1 firmware-modding scene around op1hacks is real and well-trodden, while OP-1 field hacking is far thinner and the firmware archives are now reference-only. The sample/AIF tooling is plentiful but mostly old and unmaintained.*

### Custom firmware & OS

- [op1hacks](https://github.com/op1hacks) - Primary GitHub org for OP-1 firmware hacking: repacker, docs, firmware archives, and preset tools.
- [op1repacker](https://github.com/op1hacks/op1repacker) - Unpacks, modifies, and repacks OP-1 firmware to unlock hidden iter synth, filter, and custom graphics mods. (dormant)
- [op1-fw-archive](https://github.com/op1hacks/op1-fw-archive) - Archive of (almost) all original OP-1 firmware versions for downgrade and research.
- [op1-field-fw-archive](https://github.com/op1hacks/op1-field-fw-archive) - Archive of OP-1 field firmware releases with changelog notes, useful for downgrade and study. (archived)

### Reverse engineering & docs

- [op1-docs](https://github.com/sualk/op1-docs) - Documentation and reverse-engineering research on OP-1 firmware and hardware internals.
- [sowbug/op-1-tools](https://github.com/sowbug/op-1-tools) - Reverse-engineering research and tooling on the OP-1's file formats and internals. (dormant)

### Tools & software

- [op1.fun](https://op1.fun) - Community hub to download and share 12,500+ patches, with an in-browser drum builder and macOS sync app.
- [OP1GO](https://github.com/tacoe/OP1GO) - Ultraportable Raspberry Pi Zero backup appliance for the OP-1, no computer required.
- [Xfer Records OP-1 Drum Utility](https://rekkerd.org/xfer-records-releases-op-1-drum-utility) - Free Win/Mac plugin merging 24 one-shot samples into a valid OP-1 drumkit AIF file. (dormant)
- [operator1/op1](https://github.com/operator1/op1) - Java utilities to split stereo and drumkits and pack samples into OP-1 drumkits. (dormant)
- [libop1](https://github.com/padenot/libop1) - Library plus CLI programs to manipulate AIFF files in OP-1's patch and sample format. (dormant)
- [OPluge](https://github.com/adwuard/OPluge) - Converts OP-1 AIF patches to Synthstrom Deluge XML patch format. (dormant)
- [op1-drumkit-reader](https://github.com/brentvatne/op1-drumkit-reader) - Node.js library to extract JSON drumkit metadata embedded in OP-1 drumkit AIF files. (dormant)
- [blattm/op1tools](https://github.com/blattm/op1tools) - Adds short audio previews to OP-1 patches by round-tripping them through the device over USB. (dormant)

## EP-133 K.O. II / EP-1320

*The most active third-party Teenage Engineering scene right now: people have reverse-engineered the undocumented project filesystem and SysEx protocol, and tools are still shipping in 2026.*

### Reverse engineering & docs

- [ep_133_sysex_thingy](https://github.com/garrettjwilke/ep_133_sysex_thingy) - Reverse-engineered SysEx command library and docs to manage K.O. II samples without the official tool. (WIP)
- [KOII-tips-and-tricks](https://github.com/neilbaldwin/KOII-tips-and-tricks) - Community-compiled guide of K.O. II tips and tricks distilled from Elektronauts forum threads.

### Tools & software

- [ep133-export-to-daw](https://github.com/phones24/ep133-export-to-daw) - Reverse-engineered WebMIDI tool exporting full K.O. II projects to Ableton, REAPER, DAWproject, and MIDI; hosted at ep133-to-daw.cc.
- [ep_133_sample_tool](https://github.com/garrettjwilke/ep_133_sample_tool) - Offline fork of the EP sample tool adding projects-only backup and raw SysEx debugging. (archived)
- [mcp-koii](https://github.com/benjaminr/mcp-koii) - MCP server controlling the K.O. II over MIDI so an LLM can play notes and patterns.

## Pocket Operators

*A mature, mostly quiet scene: the calculator-sized POs are cheap and beloved, but hacking centers on one perennial gap - getting MIDI/sync in and out - so most work is small hardware add-ons plus a couple of web tools, several now dormant.*

### Custom firmware & OS

- [Hanz Tech PO MIDI Adapter V3](https://github.com/Hanz-Tech/midi-adapter-v3-software) - Adapter firmware taking USB/DIN MIDI in and pressing PO buttons via GPIO.

### Tools & software

- [po-33](https://github.com/rileyjshaw/po-33) - Clean browser drag-and-drop loader that records sample banks into the PO-33 K.O.
- [Pocket Operator simulator](https://github.com/franeklubi/pocket-operator-simulator) - In-browser JavaScript emulation of the PO-20 drum machine with a working sequencer. (dormant)

### Hardware mods

- [Pocket Operator MIDI Sync](https://hackaday.io/project/10869-pocket-operator-midi-sync) - Converts MIDI sync into the click-track audio pulse a PO needs to lock tempo.
- [USB MIDI for Pocket Operator](https://hackaday.io/project/28865-usb-midi-for-teenage-engineering-pocket-operator) - DIY board adding USB MIDI and USB host (keyboard/OP-1) via soldered taps. (dormant)
- [Pocket Integrator](https://hackaday.io/project/186778-pocket-integrator) - Add-on board with tap/shake play, USB MIDI clock, battery, and SWD for firmware hacking. (dormant)

## Cross-device tools

*A small but genuinely useful cluster of tools that span two or more TE devices, mostly patch/sample converters and portable backup managers; a few are dormant single-maintainer repos.*

### Tools & software

- [teoperator](https://github.com/schollz/teoperator) - Turns any audio file into OP-1 and OP-Z drum and synth patches, with a hosted version.
- [DigiChain](https://github.com/brian3kb/digichain) - Builds and splits sample chains and kits for OP-1 Field, OP-Z, and OP-XY in the browser.
- [OP-PatchStudio](https://github.com/joseph-holland/op-patchstudio) - Open-source web app to build drum and multisample presets for both OP-XY and OP-1.
- [OP_Manager](https://github.com/adwuard/OP_Manager) - Raspberry Pi Zero handheld file manager for on-the-go backup and upload of OP-1/OP-Z patches.
- [op-patch-util](https://github.com/AlexCharlton/op-patch-util) - Rust CLI to create and modify OP-1 and OP-Z drum patches, pitch, and metadata. (dormant)
- [OP-1Z-Sample-Manager](https://github.com/romangarms/OP-1Z-Sample-Manager) - Cross-platform desktop app for managing OP-Z and OP-1 samples. (dormant)
- [mezmer](https://github.com/idroz/mezmer-app) - Live sound visualizer that works with both OP-Z and OP-XY. (dormant)

## Contributing

Found something missing or stale? See [CONTRIBUTING.md](CONTRIBUTING.md) - one-line entries, honest status, curate don't collect. Dead links are caught weekly by the [link-check workflow](.github/workflows/link-check.yml).

## License

To the extent possible under law, contributors have waived all copyright and related rights to this work under [CC0 1.0 Universal](LICENSE).

*Last reviewed: 2026-06-15.*
