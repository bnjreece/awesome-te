# awesome-te

> A curated directory of reverse-engineering, custom firmware, tools, mods, and teardowns for Teenage Engineering gear.

**Scope:** real, working, TE-specific projects only. Curate, don't collect - see [Contributing](CONTRIBUTING.md).

**Status tags:** an entry is actively maintained unless tagged `dormant` (works, but quiet) or `archived` (read-only). Everything listed is usable today - we don't list announced-but-unreleased projects.

## Contents

- [SP-1 / Stem Player](#sp-1--stem-player)
- [TP-7](#tp-7)
- [OP-XY](#op-xy)
- [OP-Z](#op-z)
- [OP-1 / OP-1 field](#op-1--op-1-field)
- [EP-133 K.O. II / EP-1320](#ep-133-ko-ii--ep-1320)
- [Pocket Operators](#pocket-operators)
- [TX-6](#tx-6)
- [OD-11 / Ortho Remote](#od-11--ortho-remote)
- [Cross-device tools](#cross-device-tools)

## SP-1 / Stem Player

### Custom firmware & OS

- [sp1-midi](https://github.com/ericlewis/sp1-midi) - Zephyr BSP/template that is the foundation for building custom SP-1 synths, MIDI controllers, or firmware.
- [sp1-tape-looper](https://github.com/chattock/sp1-tape-looper) - Four-track tape-machine looper firmware that ships a known-good recovery bin.
- [marisko](https://github.com/softmodded/marisko) - Community custom firmware plus a ready-to-use Zephyr board definition for the SP-1.
- [feldd](https://feldd.com) - Turns the SP-1 into a USB and TRS MIDI controller; map the faders and buttons to any CC or note from the browser, with per-control channels for a mixer.

### Reverse engineering & docs

- [SP-1-dev](https://github.com/timknapen/SP-1-dev) - The hub: GPIO pinout, bootloader protocol, eMMC notes, and a dev wiki for writing firmware.
- [SP-1-knowledgebase-skill](https://github.com/dot-Justin/SP-1-knowledgebase-skill) - Cited, curated SP-1 technical reference library packaged as a Claude agent skill.

### Tools & software

- [spire](https://github.com/softmodded/spire) - Renode-based SP-1 emulator that tests firmware with zero brick risk before flashing.
- [sp1-merge](https://github.com/softmodded/sp1-merge) - CLI tool to encode and merge Demucs stems into an SP-1-compatible WAV.
- [Stem Player Studio](https://github.com/humperdink13/TE-StemPlayer) - Desktop app to manage the SP-1, including a host-side Python firmware flasher.
- [SP-1 Utility](https://github.com/JT-Apps/SP-1-Utility) - Native Mac app that converts songs or four-stem folders into SP-1 WAVs and uploads them over USB-C, no Terminal or Python needed.
- [solderless.engineering](https://solderless.engineering) - Web updater that loads custom stems and flashes firmware without opening the unit.
- [yzy-stemplayer-reverse](https://github.com/leabs/yzy-stemplayer-reverse) - PyUSB scripts that fuzz the Stem Player's USB vendor requests, DFU entry, and memory.

### Teardown, flashing & recovery

- [ESP32_nRF52840_glitch](https://github.com/timknapen/ESP32_nRF52840_glitch) - ESP32 tool to read/write internal nRF52 flash over SWD/glitch, used for SP-1 recovery. `dormant`

### Community

- [TE SP-1 lines thread archive](https://github.com/dot-Justin/TE-SP-1-lines-thread-archive) - Public archive of the 846-post reverse-engineering thread, also live at sp-1.dotjust.in.
- [TE SP-1 dev (Discord)](https://discord.gg/y4V6VfHYck) - Live SP-1 firmware/software dev community the scene moved to after the lines thread closed.
- [lines TE Stem Player thread](https://llllllll.co/t/te-stem-player/66795) - The primary forum thread, now closed, where SP-1 reverse engineering happened. `archived`

## TP-7

### Reverse engineering & docs

- [TP-7 guide: going deeper](https://www.spongefile.com/tp-7-guide-going-deeper) - Independent cheat-sheet decoding the TP-7's opaque UI, multitrack, loop and cue workflows.

### Tools & software

- [tp7-midi](https://github.com/lucidyan/tp7-midi) - Web app that documents the TP-7's quirky MIDI CC behavior while driving transport, loops and cues over Web MIDI/BLE.
- [tp7-util](https://github.com/mellson/tp7-util) - macOS app to split and combine TP-7 multitrack polyWAV stems for DAW workflows.
- [TP-7-VoiceSync](https://github.com/armynante/TP-7-VoiceSync) - macOS menu bar app that auto-syncs, transcribes and files TP-7 voice memos to Apple Notes.
- [wavesync](https://github.com/pixelate/wavesync) - Ruby CLI that converts a music library to TP-7 spec and syncs it to the device over MTP.

### Teardown, flashing & recovery

- [TP-7 Disassembly Tools](https://www.printables.com/model/1478390-teenage-engineering-tp-7-disassembly-tools) - 3D-printable non-standard tools to open a TP-7, though the author warns disassembly likely bricks it. `dormant`

### Community

- [Teenage Engineering TP-7 thread (lines)](https://llllllll.co/t/teenage-engineering-tp-7/63256) - The main community hub for TP-7 workflows, tips and teardown chatter.

## OP-XY

### Reverse engineering & docs

- [kmorrill/xy-format](https://gist.github.com/kmorrill/506d69e251f225c0fffb2596c17b9db3) - Community reverse-engineering notes on the OP-XY .xy binary project format, the anchor reference for the scene.

### Tools & software

- [kmorrill/op-xy-vibing](https://github.com/kmorrill/op-xy-vibing) - AI-assisted JSON loop editor that plays to OP-XY over USB-C MIDI and exports presets.
- [buba447/OPXY-Multisample-Tool](https://github.com/buba447/OPXY-Multisample-Tool) - Python scripts to record and pack WAV/AIFF samples into OP-XY multisample presets.
- [buba447 OP-XY Drum & Multisample Patch Generator](https://buba447.github.io/opxy-drum-tool) - Hosted web generator that builds OP-XY drum kits and multisample patches from audio files.
- [sixthlaw/opxy-multisampler-preset-builder](https://github.com/sixthlaw/opxy-multisampler-preset-builder) - Browser tool to drag-drop audio into OP-XY multisampler preset folders with automatic pitch detection.
- [stembounce](https://github.com/om3opr/stembounce) - Browser tool that MIDI-solos each OP-XY track, records USB audio, and packages per-track WAV stems.
- [op-xy-drum-builder](https://github.com/niekert/op-xy-drum-builder) - Web app to assemble OP-XY drum racks from your own audio files.
- [vjxy](https://vjxy.app) - MIDI-driven live visual instrument for the OP-XY: trigger video clips from notes and steer FX with CC.
- [discepoli/op-xy-drum-preset-builder](https://github.com/discepoli/op-xy-drum-preset-builder) - Builds OP-XY drum sampler presets from a list of sample files. `dormant`
- OP-XY preset/sample format converters: [SF2 in](https://github.com/charlesvestal/sf2-to-opxy), [SFZ out](https://github.com/legsmechanical/opxy-to-sfz), [DX7 SYSEX](https://github.com/cfurrow7/dx7-opxy), [NI Maschine](https://github.com/DimaDake/maschine-multisample-to-op-xy-converter), [Logic/GarageBand kits](https://github.com/inrainbws/logic_pro_drums_for_opxy).

## OP-Z

### Reverse engineering & docs

- [libopz](https://github.com/patriciogonzalezvivo/libopz) - Unofficial C++ library to parse .opz project files and talk to the OP-Z over MIDI/SysEx.
- [z-po-project](https://github.com/lrk/z-po-project) - Reverse-engineering wiki documenting OP-Z internals, the closest thing to a protocol bible. `dormant`

### Tools & software

- [videolab](https://github.com/teenageengineering/videolab) - Official Unity toolset for building OP-Z videopaks, the foundation every custom videopak is built on.
- [connect-opz](https://github.com/xmacex/connect-opz) - Lua script to wire the OP-Z in as an audio device on the monome norns.
- [underbridge](https://github.com/BKLronin/underbridge) - Exports OP-Z patterns and projects to separate per-track audio folders for a DAW.
- [OPZ_Bounce_Puller](https://github.com/robtruckr/OPZ_Bounce_Puller) - Windows app that auto-transfers, renames, and clears .wav bounce files off the OP-Z.
- [VideolabTest](https://github.com/keijiro/VideolabTest) - Worked videolab shader/effect examples that show how to actually build a videopak. `dormant`
- [OP-Z-Videopak](https://github.com/berndpl/OP-Z-Videopak) - Ready-made collection of OP-Z videopaks to drop in or learn from. `dormant`
- [op-z-m-vave-smk-25](https://github.com/tsoop-com/op-z-m-vave-smk-25) - MIDI bindings that drive the OP-Z sequencer from a cheap M-Vave wireless controller. `dormant`
- [OPZgo](https://github.com/chrisdiana/OPZgo) - Python utility for ultra-portable OP-Z backups with no computer needed. `dormant`
- OP-Z videopaks: [Roman's collection](https://github.com/romangarms/Romans-VideoPaks), [Chords UI](https://github.com/mochreach/chords), [Tape Track FX](https://github.com/Videolab-Creators-Group/Tape-Track-Videopak).

### Hardware mods

- [OP-Z-Cube](https://github.com/MateSteinforth/OP-Z-Cube) - Arduino-driven LED light object that reacts live to the OP-Z. `dormant`

## OP-1 / OP-1 field

### Custom firmware & OS

- [op1hacks](https://github.com/op1hacks) - Primary GitHub org for OP-1 firmware hacking: repacker, docs, firmware archives, and preset tools.
- [op1repacker](https://github.com/op1hacks/op1repacker) - Unpacks, modifies, and repacks OP-1 firmware to unlock hidden iter synth, filter, and custom graphics mods.
- [op1-fw-archive](https://github.com/op1hacks/op1-fw-archive) - Archive of (almost) all original OP-1 firmware versions for downgrade and research.
- [op1REpackerGUI](https://github.com/epixjava/op1REpackerGUI) - Desktop GUI front-end for op1repacker, making OP-1 firmware mods accessible without the CLI.
- [op1-field-fw-archive](https://github.com/op1hacks/op1-field-fw-archive) - Archive of OP-1 field firmware releases with changelog notes, useful for downgrade and study. `archived`

### Reverse engineering & docs

- [op1-docs](https://github.com/sualk/op1-docs) - Documentation and reverse-engineering research on OP-1 firmware and hardware internals.
- [sowbug/op-1-tools](https://github.com/sowbug/op-1-tools) - Reverse-engineering research and tooling on the OP-1's file formats and internals. `dormant`

### Tools & software

- [op1.fun](https://op1.fun) - Community hub to download and share 12,500+ patches, with an in-browser drum builder and macOS sync app.
- [OP1GO](https://github.com/tacoe/OP1GO) - Ultraportable Raspberry Pi Zero backup appliance for the OP-1, no computer required.
- [OP1field](https://github.com/tacoe/OP1field) - Ableton Live 12 remote script giving the OP-1 Field transport, arm/mute/solo and navigation.
- [op1-lfo-hero](https://github.com/andrewralon/op1-lfo-hero) - Sends beat-synced LFO automation (pan/mute/volume) to the OP-1 Field over USB-C or BLE MIDI.
- [Xfer Records OP-1 Drum Utility](https://rekkerd.org/xfer-records-releases-op-1-drum-utility) - Free Win/Mac plugin merging 24 one-shot samples into a valid OP-1 drumkit AIF file. `dormant`
- [operator1/op1](https://github.com/operator1/op1) - Java utilities to split stereo and drumkits and pack samples into OP-1 drumkits. `dormant`
- [libop1](https://github.com/padenot/libop1) - Library plus CLI programs to manipulate AIFF files in OP-1's patch and sample format. `dormant`
- [OPluge](https://github.com/adwuard/OPluge) - Converts OP-1 AIF patches to Synthstrom Deluge XML patch format. `dormant`
- [op1-drumkit-reader](https://github.com/brentvatne/op1-drumkit-reader) - Node.js library to extract JSON drumkit metadata embedded in OP-1 drumkit AIF files. `dormant`
- [blattm/op1tools](https://github.com/blattm/op1tools) - Adds short audio previews to OP-1 patches by round-tripping them through the device over USB. `dormant`

### Teardown, flashing & recovery

- [iFixit OP-1 repair guides](https://www.ifixit.com/Device/Teenage_Engineering_OP-1) - Eight step-by-step teardown/repair guides: battery, display, keyboard, connector board, flex cable.
- [op1dumps](https://github.com/Tolsi/op1dumps) - Flash/OTP dumps, schematic, and bootloader for replacing a dead OP-1 processor or flash chip. `dormant`

## EP-133 K.O. II / EP-1320

### Reverse engineering & docs

- [KOII-tips-and-tricks](https://github.com/neilbaldwin/KOII-tips-and-tricks) - Community-compiled guide of K.O. II tips and tricks distilled from Elektronauts forum threads.
- [ep_133_sysex_thingy](https://github.com/garrettjwilke/ep_133_sysex_thingy) - Reverse-engineered SysEx command library and docs to manage K.O. II samples without the official tool. `dormant`

### Tools & software

- [ep133-export-to-daw](https://github.com/phones24/ep133-export-to-daw) - Reverse-engineered WebMIDI tool exporting full K.O. II projects to Ableton, REAPER, DAWproject, and MIDI; hosted at ep133-to-daw.cc.
- [mcp-koii](https://github.com/benjaminr/mcp-koii) - MCP server controlling the K.O. II over MIDI so an LLM can play notes and patterns.
- [ep133-krate](https://github.com/icherniukh/ep133-krate) - CLI and terminal-UI sample manager built on a reverse-engineered SysEx protocol.
- [knockout](https://github.com/gabriel-roth/knockout) - Electron desktop sample manager that imports WAVs and exports .ppak projects and .pak backups.
- [ep133-ppak](https://github.com/ZacharySBrown/ep133-ppak) - Python library and CLI to write valid .ppak sample-mode and song-mode project files from JSON.
- [Cornerman for K.O. II](https://apps.apple.com/us/app/cornerman-for-k-o-ii/id6499280264) - iOS app that backs up the K.O. II offline, without TE's web tool.
- [EP Toolkit](https://eptoolkit.ep133-to-daw.cc) - Native EP-133/1320/40 app: project export to DAWs, full sample management, CLAP processing, and device backups.
- [AudioBatchConverter](https://github.com/JanSchulten/AudioBatchConverter) - Batch-prepares audio samples for the K.O. II and exports sample chains for the PO-33.
- [EP-PatchStudio](https://ep-patch.studio) - Rust desktop app for EP-133/1320/40: device management, multisample editor, MIDI auto-sampler, and audio editing; pay-what-you-want.
- [ep_133_sample_tool](https://github.com/garrettjwilke/ep_133_sample_tool) - Offline fork of the EP sample tool adding projects-only backup and raw SysEx debugging. `archived`

## Pocket Operators

### Custom firmware & OS

- [Hanz Tech PO MIDI Adapter V3](https://github.com/Hanz-Tech/midi-adapter-v3-software) - Adapter firmware taking USB/DIN MIDI in and pressing PO buttons via GPIO.

### Tools & software

- [po-33](https://github.com/rileyjshaw/po-33) - Clean browser drag-and-drop loader that records sample banks into the PO-33 K.O.
- [Pocket Operator simulator](https://github.com/franeklubi/pocket-operator-simulator) - In-browser JavaScript emulation of the PO-20 drum machine with a working sequencer. `dormant`

### Hardware mods

- [Hanz Tech PO MIDI Adapter V3 (hardware)](https://github.com/Hanz-Tech/midi-adapter-v3-hardware) - KiCad PCB and pogo-pin cover CAD for the PO MIDI adapter; companion to its firmware.
- [Pocket Operator MIDI Sync](https://hackaday.io/project/10869-pocket-operator-midi-sync) - Converts MIDI sync into the click-track audio pulse a PO needs to lock tempo. `dormant`
- [USB MIDI for Pocket Operator](https://hackaday.io/project/28865-usb-midi-for-teenage-engineering-pocket-operator) - DIY board adding USB MIDI and USB host (keyboard/OP-1) via soldered taps. `dormant`
- [Pocket Integrator](https://hackaday.io/project/186778-pocket-integrator) - Add-on board with tap/shake play, USB MIDI clock, battery, and SWD for firmware hacking. `dormant`

## TX-6

### Reverse engineering & docs

- [tx-6-midi-events](https://github.com/darnfish/tx-6-midi-events) - Reverse-engineered TX-6 BLE MIDI event map plus a connect.js that logs live events. `dormant`

### Tools & software

- [tx6 (web remote)](https://github.com/psimyn/tx6) - Live web PWA remote controlling the TX-6 over Web MIDI (BLE and USB), with an LFO engine.

## OD-11 / Ortho Remote

### Reverse engineering & docs

- [node-od11](https://github.com/Marcocanc/node-od11) - TypeScript Node library to interface with and control the OD-11 cloud speaker. `archived`

### Tools & software

- [OD11-remote](https://github.com/paolocamerin/OD11-remote) - Node app controlling OD-11 volume via a Senic Nuimo BLE controller over its WebSocket API.
- [ortho-remote-mac](https://github.com/araa47/ortho-remote-mac) - macOS tool mapping the Ortho Remote knob to volume, play/pause, and Spotify navigation.

## Cross-device tools

### Tools & software

- [teoperator](https://github.com/schollz/teoperator) - Turns any audio file into OP-1 and OP-Z drum and synth patches, with a hosted version.
- [DigiChain](https://github.com/brian3kb/digichain) - Builds and splits sample chains and kits for OP-1 Field, OP-Z, and OP-XY in the browser.
- [OP-PatchStudio](https://github.com/joseph-holland/op-patchstudio) - Open-source web app to build drum and multisample presets for both OP-XY and OP-1.
- [OP_Manager](https://github.com/adwuard/OP_Manager) - Raspberry Pi Zero handheld file manager for on-the-go backup and upload of OP-1/OP-Z patches.
- [OP-1Z-Sample-Manager](https://github.com/romangarms/OP-1Z-Sample-Manager) - Cross-platform desktop app for managing OP-Z and OP-1 samples.
- [TEKit](https://github.com/ericlewis/TEKit) - Swift package controlling TE devices (OP-Z/TP-7/OB-4/OD-11) over BLE, USB, and WebSocket.
- [field-remote](https://github.com/jwamin/field-remote) - SwiftUI iOS BLE MIDI remote for TE field gear, with control panels for TX-6 and TP-7.
- [MTVP](https://mtvp.app) - Free iOS app that plays video locked to your OP synths' MIDI transport and timecode.
- [op-patch-util](https://github.com/AlexCharlton/op-patch-util) - Rust CLI to create and modify OP-1 and OP-Z drum patches, pitch, and metadata. `dormant`
- [mezmer](https://github.com/idroz/mezmer-app) - Live sound visualizer that works with both OP-Z and OP-XY. `dormant`

### Hardware mods

- [TEcases](https://tecases.com) - Handmade protective cases sold for OP-1 field, OP-XY, EP-series, TP-7, TX-6, Pocket Operators, and OB-4.

### Community

- [op-forums.com](https://op-forums.com) - The primary active TE community forum and the hub where most firmware and tool research starts.

## Credits & inspiration

This directory exists because a few people did the hard reverse engineering and documented it carefully. Particular thanks to:

- **[TimK (timknapen)](https://github.com/timknapen)** - the [SP-1-dev](https://github.com/timknapen/SP-1-dev) hardware reverse-engineering hub and wiki the Stem Player scene is built on.
- **[dot-Justin](https://github.com/dot-Justin)** - the [lines-thread archive](https://github.com/dot-Justin/TE-SP-1-lines-thread-archive) and the cited [SP-1 knowledgebase](https://github.com/dot-Justin/SP-1-knowledgebase-skill) that set the bar for honest, sourced documentation this list aims to live up to.

...and every contributor named throughout the linked projects.

## Contributing

Found something missing or stale? See [CONTRIBUTING.md](CONTRIBUTING.md) - one-line entries, honest status, curate don't collect. Dead links are caught weekly by the [link-check workflow](.github/workflows/link-check.yml).

## License

To the extent possible under law, contributors have waived all copyright and related rights to this work under [CC0 1.0 Universal](LICENSE).

*Last reviewed: 2026-06-15.*
