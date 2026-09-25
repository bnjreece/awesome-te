# awesome-te

> A curated directory of reverse-engineering, custom firmware, tools, mods, and teardowns for Teenage Engineering gear.

**Scope:** real, working, TE-specific projects only. Curate, don't collect - see [Contributing](CONTRIBUTING.md).

**Status:** 🟢 active (updated in the last 12 months) · 🟡 dormant (works, but quiet for 12+ months) · 🔴 archived (read-only / explicitly archived). Everything listed is usable today - we don't list announced-but-unreleased projects.

## Contents

- [SP-1 / Stem Player](#sp-1--stem-player)
- [TP-7](#tp-7)
- [OP-XY](#op-xy)
- [OP-Z](#op-z)
- [OP-1 / OP-1 field](#op-1--op-1-field)
- [EP series (K.O. II, EP-1320, EP-40, EP-136)](#ep-series-ko-ii-ep-1320-ep-40-ep-136)
- [EP-2350 Ting FX](#ep-2350-ting-fx)
- [Pocket Operators](#pocket-operators)
- [TX-6](#tx-6)
- [OD-11 / Ortho Remote](#od-11--ortho-remote)
- [Choir](#choir)
- [Cross-device tools](#cross-device-tools)

## SP-1 / Stem Player

### Custom firmware & OS

- 🟢 [sp1-midi](https://github.com/ericlewis/sp1-midi) - Zephyr BSP/template that is the foundation for building custom SP-1 synths, MIDI controllers, or firmware.
- 🟢 [sp1-tape-looper](https://github.com/chattock/sp1-tape-looper) - Four-track tape-machine looper firmware that ships a known-good recovery bin.
- 🟢 [marisko](https://github.com/softmodded/marisko) - Community custom firmware plus a ready-to-use Zephyr board definition for the SP-1.
- 🟢 [feldd](https://feldd.com) - Turns the SP-1 into a USB, Bluetooth and TRS MIDI controller; map the faders and buttons to any CC or note from the browser, with per-control channels for a mixer.
- 🟢 [sp1-usb-audio](https://github.com/ryanmgilmore/sp1-usb-audio) - Reusable UAC2 code and a demo firmware that let custom SP-1 firmware stream class-compliant 48 kHz USB audio to a computer.

### Reverse engineering & docs

- 🟢 [SP-1-dev](https://github.com/timknapen/SP-1-dev) - The hub: GPIO pinout, bootloader protocol, eMMC notes, and a dev wiki for writing firmware.
- 🟢 [SP-1-knowledgebase-skill](https://github.com/dot-Justin/SP-1-knowledgebase-skill) - Cited, curated SP-1 technical reference library packaged as a Claude agent skill.
- 🟢 [SP-1 Firmware Dev Field Guide](https://marcabisamra.github.io/sp1-firmware-guide) - Cited, step-by-step site that takes you from a sealed SP-1 to building and flashing your own Zephyr firmware.

### Tools & software

- 🟢 [spire](https://github.com/softmodded/spire) - Renode-based SP-1 emulator that tests firmware with zero brick risk before flashing.
- 🟢 [sp1-merge](https://github.com/softmodded/sp1-merge) - CLI tool to encode and merge Demucs stems into an SP-1-compatible WAV.
- 🟢 [Stem Player Studio](https://github.com/humperdink13/TE-StemPlayer) - Desktop app to manage the SP-1, including a host-side Python firmware flasher.
- 🟢 [SP-1 Utility](https://github.com/JT-Apps/SP-1-Utility) - Native Mac app that converts songs or four-stem folders into SP-1 WAVs and uploads them over USB-C, no Terminal or Python needed.
- 🟢 [solderless.engineering](https://solderless.engineering) - Web updater that loads custom stems and flashes firmware without opening the unit.
- 🟢 [yzy-stemplayer-reverse](https://github.com/leabs/yzy-stemplayer-reverse) - PyUSB scripts that fuzz the Stem Player's USB vendor requests, DFU entry, and memory.
- 🟢 More SP-1 stem loaders: [rome](https://github.com/softmodded/rome) (marisko's flashing and stem CLI), [sp1-loader](https://github.com/sh4tteredd/sp1-loader) (Python CLI and GUI).

### Teardown, flashing & recovery

- 🟡 [ESP32_nRF52840_glitch](https://github.com/timknapen/ESP32_nRF52840_glitch) - ESP32 tool to read/write internal nRF52 flash over SWD/glitch, used for SP-1 recovery.

### Community

- 🟢 [TE SP-1 lines thread archive](https://github.com/dot-Justin/TE-SP-1-lines-thread-archive) - Public archive of the 846-post reverse-engineering thread, also live at sp-1.dotjust.in.
- 🟢 [TE SP-1 dev (Discord)](https://discord.gg/y4V6VfHYck) - Live SP-1 firmware/software dev community the scene moved to after the lines thread closed.
- 🟢 [SP-1 firmware thread (Elektronauts)](https://www.elektronauts.com/t/sp-1-stem-player-firmware-new-things/252617) - Busy public thread where SP-1 firmware releases, betas, and flashing help surface now that lines is closed.
- 🔴 [lines TE Stem Player thread](https://llllllll.co/t/te-stem-player/66795) - The primary forum thread, now closed, where SP-1 reverse engineering happened.

## TP-7

### Reverse engineering & docs

- 🟢 [TP-7 guide: going deeper](https://www.spongefile.com/tp-7-guide-going-deeper) - Independent cheat-sheet decoding the TP-7's opaque UI, multitrack, loop and cue workflows.

### Tools & software

- 🟢 [tp7-midi](https://github.com/lucidyan/tp7-midi) - Web app that documents the TP-7's quirky MIDI CC behavior while driving transport, loops and cues over Web MIDI/BLE.
- 🟢 [TP-7-VoiceSync](https://github.com/armynante/TP-7-VoiceSync) - macOS menu bar app that auto-syncs, transcribes and files TP-7 voice memos to Apple Notes.
- 🟢 [wavesync](https://github.com/pixelate/wavesync) - Ruby CLI that converts a music library to TP-7 spec and syncs it to the device over MTP.
- 🟢 [tp7-station](https://github.com/krystalmaria/tp7-station) - Signed macOS app that auto-syncs the TP-7, transcribes memos on-device, and writes edited cue points back to the recorder.
- 🟢 More TP-7 memo sync and control apps: [TP-7 Manager](https://github.com/joshualexanderl/TP-7-Manager), [TP7 Vibe Deck](https://github.com/PacoZhou1/tp7-vibe-deck) (TP-7 as a Mac control surface).
- 🟡 [tp7-util](https://github.com/mellson/tp7-util) - macOS app to split and combine TP-7 multitrack polyWAV stems for DAW workflows.

### Teardown, flashing & recovery

- 🟢 [TP-7 Disassembly Tools](https://www.printables.com/model/1478390-teenage-engineering-tp-7-disassembly-tools) - 3D-printable non-standard tools to open a TP-7, though the author warns disassembly likely bricks it.

### Community

- 🟢 [Teenage Engineering TP-7 thread (lines)](https://llllllll.co/t/teenage-engineering-tp-7/63256) - The main community hub for TP-7 workflows, tips and teardown chatter.

## OP-XY

### Reverse engineering & docs

- 🟢 [kmorrill/xy-format](https://github.com/kmorrill/xy-format) - Byte-exact decode of the OP-XY .xy project format with Python tools to inspect, edit, and generate projects, the anchor reference for the scene.

### Tools & software

- 🟢 [kmorrill/op-xy-vibing](https://github.com/kmorrill/op-xy-vibing) - AI-assisted JSON loop editor that plays to OP-XY over USB-C MIDI and exports presets.
- 🟢 [sixthlaw/opxy-multisampler-preset-builder](https://github.com/sixthlaw/opxy-multisampler-preset-builder) - Browser tool to drag-drop audio into OP-XY multisampler preset folders with automatic pitch detection.
- 🟢 [stembounce](https://github.com/om3opr/stembounce) - Browser tool that MIDI-solos each OP-XY track, records USB audio, and packages per-track WAV stems.
- 🟢 [vjxy](https://vjxy.app) - MIDI-driven live visual instrument for the OP-XY: trigger video clips from notes and steer FX with CC.
- 🟢 [OPXY.APP](https://opxy.app) - Browser tool that renames and relinks OP-XY samples across every project, flags truncated filenames, and batch-downsamples to free space.
- 🟢 [XY Buddy](https://xybuddy.xyz) - Web utility that turns MIDI files into OP-XY projects and exports .xy patterns back to MIDI.
- 🟢 [opxy-deck](https://github.com/kazuochi/opxy-deck) - Turns the OP-XY into a macro deck for AI coding agents, with a full map of its controller-mode MIDI output.
- 🟢 OP-XY preset/sample format converters: [SF2 in](https://github.com/charlesvestal/sf2-to-opxy), [SFZ out](https://github.com/legsmechanical/opxy-to-sfz), [DX7 SYSEX](https://github.com/cfurrow7/dx7-opxy), [NI Maschine](https://github.com/DimaDake/maschine-multisample-to-op-xy-converter), [Logic/GarageBand kits](https://github.com/inrainbws/logic_pro_drums_for_opxy), [REX/sliced loops](https://github.com/g-lok/chirashi).
- 🟡 [OP-PatchStudio](https://op-patch.studio) - Free legacy browser app for OP-XY drum and multisample presets, with OP-1 drum-preset import.
- 🟡 [buba447/OPXY-Multisample-Tool](https://github.com/buba447/OPXY-Multisample-Tool) - Python scripts to record and pack WAV/AIFF samples into OP-XY multisample presets.
- 🟡 [buba447 OP-XY Drum & Multisample Patch Generator](https://buba447.github.io/opxy-drum-tool) - Hosted web generator that builds OP-XY drum kits and multisample patches from audio files.
- 🟡 [op-xy-drum-builder](https://github.com/niekert/op-xy-drum-builder) - Web app to assemble OP-XY drum racks from your own audio files.
- 🟡 [discepoli/op-xy-drum-preset-builder](https://github.com/discepoli/op-xy-drum-preset-builder) - Builds OP-XY drum sampler presets from a list of sample files.

## OP-Z

### Reverse engineering & docs

- 🟢 [OP-Z SysEx](https://github.com/kmorrill/op-z-sysex) - Device-proven docs for OP-Z SysEx, StateSync, and file transfer, plus Python tools for guarded project and sample writes.
- 🟡 [libopz](https://github.com/patriciogonzalezvivo/libopz) - Unofficial C++ library to parse .opz project files and talk to the OP-Z over MIDI/SysEx.
- 🟡 [z-po-project](https://github.com/lrk/z-po-project) - Reverse-engineering wiki documenting OP-Z internals, the original community protocol reference.

### Tools & software

- 🟡 [videolab](https://github.com/teenageengineering/videolab) - Official Unity toolset for building OP-Z videopaks, the foundation every custom videopak is built on.
- 🟡 [connect-opz](https://github.com/xmacex/connect-opz) - Lua script to wire the OP-Z in as an audio device on the monome norns.
- 🟡 [underbridge](https://github.com/BKLronin/underbridge) - Exports OP-Z patterns and projects to separate per-track audio folders for a DAW.
- 🟡 [OPZ_Bounce_Puller](https://github.com/robtruckr/OPZ_Bounce_Puller) - Windows app that auto-transfers, renames, and clears .wav bounce files off the OP-Z.
- 🟡 [VideolabTest](https://github.com/keijiro/VideolabTest) - Worked videolab shader/effect examples that show how to actually build a videopak.
- 🟡 [OP-Z-Videopak](https://github.com/berndpl/OP-Z-Videopak) - Ready-made collection of OP-Z videopaks to drop in or learn from.
- 🟡 [op-z-m-vave-smk-25](https://github.com/tsoop-com/op-z-m-vave-smk-25) - MIDI bindings that drive the OP-Z sequencer from a cheap M-Vave wireless controller.
- 🟡 [OPZgo](https://github.com/chrisdiana/OPZgo) - Python utility for ultra-portable OP-Z backups with no computer needed.
- 🟡 OP-Z videopaks: [Roman's collection](https://github.com/romangarms/Romans-VideoPaks), [Chords UI](https://github.com/mochreach/chords), [Tape Track FX](https://github.com/Videolab-Creators-Group/Tape-Track-Videopak).

### Hardware mods

- 🟡 [OP-Z-Cube](https://github.com/MateSteinforth/OP-Z-Cube) - Arduino-driven LED light object that reacts live to the OP-Z.

## OP-1 / OP-1 field

### Custom firmware & OS

- 🟢 [op1hacks](https://github.com/op1hacks) - Primary GitHub org for OP-1 firmware hacking: repacker, docs, firmware archives, and preset tools.
- 🟢 [op1repacker](https://github.com/op1hacks/op1repacker) - Unpacks, modifies, and repacks OP-1 firmware to unlock hidden iter synth, filter, and custom graphics mods.
- 🟢 [op1REpackerGUI](https://github.com/epixjava/op1REpackerGUI) - Desktop GUI front-end for op1repacker, making OP-1 firmware mods accessible without the CLI.
- 🟡 [op1-fw-archive](https://github.com/op1hacks/op1-fw-archive) - Archive of (almost) all original OP-1 firmware versions for downgrade and research.
- 🟡 [op1-glitter](https://github.com/Nanobot567/op1-glitter) - Custom color themes for the original OP-1, patched into its firmware from a JSON file via op1repacker.
- 🟡 [op1-field-fw-archive](https://github.com/op1hacks/op1-field-fw-archive) - Archive of OP-1 field firmware releases with changelog notes, useful for downgrade and study.

### Reverse engineering & docs

- 🟢 [te-op1](https://github.com/jstnfst/te-op1) - Maps OP-1 field synth patch parameters across 15 engines, 9 effects, and 6 LFOs, with a C tool that dumps and builds .aif patches.
- 🟡 [op1-docs](https://github.com/sualk/op1-docs) - Documentation and reverse-engineering research on OP-1 firmware and hardware internals.
- 🟡 [sowbug/op-1-tools](https://github.com/sowbug/op-1-tools) - Reverse-engineering research and tooling on the OP-1's file formats and internals.

### Tools & software

- 🟢 [op1.fun](https://op1.fun) - Community hub to download and share 12,500+ patches, with an in-browser drum builder and macOS sync app.
- 🟢 [op1-lfo-hero](https://github.com/andrewralon/op1-lfo-hero) - Sends beat-synced LFO automation (pan/mute/volume) to the OP-1 Field over USB-C or BLE MIDI, also as an iOS and Mac app.
- 🟢 [op1microtonal](https://github.com/robinmeier/op1microtonal) - Browser tool that bakes Scala microtonal scales into OP-1 drum patches for exact tuning beyond semitones.
- 🟡 [OP1GO](https://github.com/tacoe/OP1GO) - Ultraportable Raspberry Pi Zero backup appliance for the OP-1, no computer required.
- 🟡 [OP1field](https://github.com/tacoe/OP1field) - Ableton Live 12 remote script giving the OP-1 Field transport, arm/mute/solo and navigation.
- 🟡 [OP-1 Tape Slicer](https://www.constellates.com/op-1-tape-slicer) - Browser tool that exports every clip on an OP-1 field tape as its own WAV.
- 🟡 [Xfer Records OP-1 Drum Utility](https://xferrecords.com/freeware) - Free Win/Mac plugin merging 24 one-shot samples into a valid OP-1 drumkit AIF file.
- 🟡 [operator1/op1](https://github.com/operator1/op1) - Java utilities to split stereo and drumkits and pack samples into OP-1 drumkits.
- 🟡 [libop1](https://github.com/padenot/libop1) - Library plus CLI programs to manipulate AIFF files in OP-1's patch and sample format.
- 🟡 [OPluge](https://github.com/adwuard/OPluge) - Converts OP-1 AIF patches to Synthstrom Deluge XML patch format.
- 🟡 [op1-drumkit-reader](https://github.com/brentvatne/op1-drumkit-reader) - Node.js library to extract JSON drumkit metadata embedded in OP-1 drumkit AIF files.
- 🟡 [blattm/op1tools](https://github.com/blattm/op1tools) - Adds short audio previews to OP-1 patches by round-tripping them through the device over USB.

### Teardown, flashing & recovery

- 🟡 [iFixit OP-1 repair guides](https://www.ifixit.com/Device/Teenage_Engineering_OP-1) - Twelve step-by-step teardown/repair guides: battery, display, keyboard, connector board, flex cable.
- 🟡 [op1dumps](https://github.com/Tolsi/op1dumps) - Flash/OTP dumps, schematic, and bootloader for replacing a dead OP-1 processor or flash chip.

## EP series (K.O. II, EP-1320, EP-40, EP-136)

### Custom firmware & OS

- 🟢 [ep-unity](https://github.com/seajaysec/ep-unity) - Browser WebMIDI tool that cross-flashes between K.O. II and EP-40 Riddim firmware by rewriting four SKU bytes, with backups; unsupported and can brick.

### Reverse engineering & docs

- 🟢 [EP SysEx](https://github.com/kmorrill/ep-series-sysex) - Capture-verified docs for the shared EP-133/EP-40 SysEx protocol and project format, with a JSON project compiler and hardware tools.
- 🟢 [KOII-tips-and-tricks](https://github.com/neilbaldwin/KOII-tips-and-tricks) - Community-compiled guide of K.O. II tips and tricks distilled from Elektronauts forum threads.
- 🟢 [EP-133 cheat sheet](https://josephharrington.github.io/ep133-cheatsheet) - Searchable, printable one-page reference for K.O. II button combos, system settings, and modes.
- 🟢 [Riddim + Ting guide](https://ourtinyapps.github.io/riddim-n-ting) - Interactive EP-40 and EP-2350 button map: tap a combo on the drawn panel to see what it does.
- 🟢 [EP-136 MIDI CC map](https://gist.github.com/GOROman/9d47019539823b119c663e1bb1034445) - Device-tested map of the K.O. Sidekick's MIDI CCs, channels, and relative encoder format for building controller mappings.
- 🟡 [ep_133_sysex_thingy](https://github.com/garrettjwilke/ep_133_sysex_thingy) - Reverse-engineered SysEx command library and docs to manage K.O. II samples without the official tool.

### Tools & software

- 🟢 [ep133-export-to-daw](https://github.com/phones24/ep133-export-to-daw) - Reverse-engineered WebMIDI tool exporting full K.O. II projects to Ableton, REAPER, DAWproject, and MIDI; hosted at ep133-to-daw.cc.
- 🟢 [ep133-krate](https://github.com/icherniukh/ep133-krate) - CLI and terminal-UI sample manager built on a reverse-engineered SysEx protocol.
- 🟢 [ep133-ppak](https://github.com/ZacharySBrown/ep133-ppak) - Python library and CLI to write valid .ppak sample-mode and song-mode project files from JSON.
- 🟢 [EP Toolkit](https://eptoolkit.ep133-to-daw.cc) - Native EP-133/1320/40 app: project export to DAWs, full sample management, CLAP processing, and device backups.
- 🟢 [AudioBatchConverter](https://github.com/JanSchulten/AudioBatchConverter) - Batch-prepares audio samples for the K.O. II and exports sample chains for the PO-33.
- 🟢 [EP-PatchStudio](https://ep-patch.studio) - Rust desktop app for EP-133/1320/40: device management, multisample editor, MIDI auto-sampler, and audio editing; pay-what-you-want.
- 🟢 [Best Friend](https://epbf.app) - Companion app for EP-133, EP-40, and EP-1320 on iPhone, iPad, and Mac that shows scenes and bounces real per-pad stems from the hardware.
- 🟢 More EP tools: [ko2-io](https://github.com/trusch/ko2-io) (Linux CLI and FUSE mount), [PunchKit](https://punchkit.dev) (iOS kit builder and backups), [EP Audio Editor](https://www.mediachance.com/epaudioeditor) (Windows, EP-40 multisamples).
- 🟢 [mcp-koii](https://github.com/benjaminr/mcp-koii) - MCP server controlling the K.O. II over MIDI so an LLM can play notes and patterns.
- 🟢 More K.O. II MCP servers: [ep133-mcp](https://github.com/wil-gerard/ep133-mcp) (samples, kits, .ppak projects), [kobox](https://github.com/yangyue1974/kobox) (pads and scales).
- 🟡 [Cornerman for K.O. II](https://apps.apple.com/us/app/cornerman-for-k-o-ii/id6499280264) - iOS app that backs up the K.O. II offline, without TE's web tool.
- 🔴 [ep_133_sample_tool](https://github.com/garrettjwilke/ep_133_sample_tool) - Offline fork of the EP sample tool adding projects-only backup and raw SysEx debugging.

## EP-2350 Ting FX

### Custom firmware & OS

- 🟢 [CircuitPython for EP-2350](https://circuitpython.org/board/teenage_engineering_ep2350) - Official CircuitPython build that replaces the Ting's stock MicroPython firmware, reversible by flashing TE's firmware back.

### Reverse engineering & docs

- 🟢 [open-ting](https://github.com/au42/open-ting) - MicroPython and binary dumps, docs, and drag-and-drop examples for advanced features out of the box.

### Tools & software

- 🟢 [tink-agent](https://github.com/tajchert/tink-agent) - macOS menu-bar app that turns the Ting into push-to-talk plus eight button macros for AI coding agents, signaled by tones over line-out.
- 🟢 [EP-2350 config editor](https://tadao314.github.io/ep2350-config-editor) - Offline single-file editor for the Ting's config.json that enforces effect ranges and remaps modulation when you reorder chains.
- 🟢 More Ting push-to-talk tools: [tingle](https://github.com/tutorintelligence/tingle), [ting-bridge](https://github.com/l7073a/ting-bridge), [fx-mic-claude](https://github.com/migueldelag/fx-mic-claude), [reasoning-ting](https://github.com/jof/reasoning-ting), [FX Talk](https://github.com/bjg4/fx-talk).
- 🟢 More Ting config tools: [fx-mic-tool](https://github.com/oxo-yuta/fx-mic-tool) (validator and live audio preview), [Adafruit config tool](https://github.com/adafruit/TE_EP2350_Config_Tool) (for the CircuitPython demo).

### Teardown, flashing & recovery

- 🟢 [Hacking the EP-2350 Ting (Adafruit)](https://learn.adafruit.com/hacking-the-teenage-engineering-ep-2350-ting) - Teardown, reverse-engineered pinout, and step-by-step CircuitPython flashing, plus a demo approximating the stock firmware.

## Pocket Operators

### Custom firmware & OS

- 🟡 [Hanz Tech PO MIDI Adapter V3](https://github.com/Hanz-Tech/midi-adapter-v3-software) - Adapter firmware taking USB/DIN MIDI in and pressing PO buttons via GPIO.

### Reverse engineering & docs

- 🟢 [libpo32](https://github.com/ericlewis/libpo32) - Portable C99 reimplementation of the PO-32 Tonic's acoustic modem and drum voice, so software can build and send patches and patterns.

### Tools & software

- 🟢 [po-12](https://github.com/ulnd/po-12) - Installable browser emulation of the PO-12 rhythm for learning the sequencer without the hardware.
- 🟡 [po-33](https://github.com/rileyjshaw/po-33) - Clean browser drag-and-drop loader that records sample banks into the PO-33 K.O.
- 🟡 [Pocket Operator simulator](https://github.com/franeklubi/pocket-operator-simulator) - In-browser JavaScript emulation of the PO-20 drum machine with a working sequencer.

### Hardware mods

- 🟡 [Hanz Tech PO MIDI Adapter V3 (hardware)](https://github.com/Hanz-Tech/midi-adapter-v3-hardware) - KiCad PCB and pogo-pin cover CAD for the PO MIDI adapter; companion to its firmware.
- 🟡 [Pocket Operator MIDI Sync](https://hackaday.io/project/10869-pocket-operator-midi-sync) - Converts MIDI sync into the click-track audio pulse a PO needs to lock tempo.
- 🟡 [USB MIDI for Pocket Operator](https://hackaday.io/project/28865-usb-midi-for-teenage-engineering-pocket-operator) - DIY board adding USB MIDI and USB host (keyboard/OP-1) via soldered taps.
- 🟡 [Pocket Integrator](https://hackaday.io/project/186778-pocket-integrator) - Add-on board with tap/shake play, USB MIDI clock, battery, and SWD for firmware hacking.
- 🟡 [pocket-operator-eurorack](https://github.com/rallen-device/pocket-operator-eurorack) - KiCad board with gerbers that mounts a Pocket Operator in 14HP of Eurorack with separate clock and audio jacks.

### Teardown, flashing & recovery

- 🟡 [Fix Pocket Operator buttons (iFixit)](https://www.ifixit.com/Guide/How+to+Fix+the+Buttons+of+a+Pocket+Operator/141451) - Five-step guide to reviving unresponsive PO buttons, a common fault on secondhand units.

### Community

- 🟢 [pocketoperations.com](https://pocketoperations.com) - Long-running fan hub indexing PO cases, cheatsheets, apps, hardware add-ons, samples, and tutorials.

## TX-6

### Reverse engineering & docs

- 🟡 [tx-6-midi-events](https://github.com/darnfish/tx-6-midi-events) - Reverse-engineered TX-6 BLE MIDI event map plus a connect.js that logs live events.

### Tools & software

- 🟢 [tx6 (web remote)](https://github.com/psimyn/tx6) - Live web PWA remote controlling the TX-6 over Web MIDI (BLE and USB), with an LFO engine.

## OD-11 / Ortho Remote

### Reverse engineering & docs

- 🟡 [ortho-remote-node](https://github.com/happycodelucky/ortho-remote-node) - TypeScript npm library exposing the Ortho Remote's BLE-MIDI rotation and button events for your own projects.
- 🔴 [node-od11](https://github.com/Marcocanc/node-od11) - TypeScript Node library to interface with and control the OD-11 cloud speaker.

### Tools & software

- 🟢 [OD11-remote](https://github.com/paolocamerin/od11-remote) - Node app controlling OD-11 volume via a Senic Nuimo BLE controller over its WebSocket API.
- 🟢 [ortho-remote-mac](https://github.com/araa47/ortho-remote-mac) - macOS tool mapping the Ortho Remote knob to volume, play/pause, and Spotify navigation.
- 🟢 [ha-orthoplay](https://github.com/vibrog/ha-orthoplay) - Home Assistant integration giving the OD-11 local control of volume, sources, and playback over its WebSocket API.

## Choir

### Reverse engineering & docs

- 🟡 [Choirama](https://github.com/jetztgradnet/Choirama) - Community findings on the Choir dolls, from voice ranges and BLE MIDI pairing to the consonant and vowel CCs that make them sing.

### Tools & software

- 🟢 [talking-with-a-choir](https://github.com/tiny-factories/talking-with-a-choir) - Mac app that turns typed text into consonant and vowel MIDI CCs so the Choir dolls sing your words.

## Cross-device tools

### Tools & software

- 🟢 [DigiChain](https://github.com/brian3kb/digichain) - Builds and splits sample chains and kits for OP-1 Field, OP-Z, and OP-XY in the browser.
- 🟢 [OP-1Z-Sample-Manager](https://github.com/romangarms/OP-1Z-Sample-Manager) - Cross-platform desktop app for managing OP-Z and OP-1 samples.
- 🟢 [TEKit](https://github.com/ericlewis/TEKit) - Swift package controlling TE devices (OP-Z/TP-7/OB-4/OD-11) over BLE, USB, and WebSocket.
- 🟢 [field-remote](https://github.com/jwamin/field-remote) - SwiftUI iOS BLE MIDI remote for TE field gear, with control panels for TX-6 and TP-7.
- 🟢 [MTVP](https://mtvp.app) - Free iOS and Android app that plays video locked to your OP synths' MIDI transport and timecode.
- 🟢 [Studio Field](https://studiofield.app) - Paid companion that backs up and transfers content across TE devices, including OP-1 field and OP-XY straight from an iPhone.
- 🟢 More sample and kit builders: [TRKLS](https://trkls.net) (OP-1, OP-1 field, OP-Z, EP-133), [Earthwire](https://earthwire.space) (OP-1 field kits from Freesound and Xeno-canto).
- 🟢 [op-patch-util](https://github.com/AlexCharlton/op-patch-util) - Rust CLI to create and modify OP-1 and OP-Z drum patches, pitch, and metadata.
- 🟡 [teoperator](https://github.com/schollz/teoperator) - Turns any audio file into OP-1 and OP-Z drum and synth patches, with a hosted version.
- 🟡 [OP_Manager](https://github.com/adwuard/OP_Manager) - Raspberry Pi Zero handheld file manager for on-the-go backup and upload of OP-1/OP-Z patches.
- 🟡 [mezmer](https://github.com/idroz/mezmer-app) - Live sound visualizer that works with both OP-Z and OP-XY.

### Hardware mods

- 🟢 [TEcases](https://tecases.com) - Handmade protective cases sold for OP-1 field, OP-XY, EP-series, TP-7, TX-6, CM-15, Pocket Operators, and OB-4.

### Community

- 🟢 [op-forums.com](https://op-forums.com) - The primary active TE community forum and the hub where most firmware and tool research starts.

## Credits & inspiration

This directory exists because a few people did the hard reverse engineering and documented it carefully. Particular thanks to:

- **[TimK (timknapen)](https://github.com/timknapen)** - the [SP-1-dev](https://github.com/timknapen/SP-1-dev) hardware reverse-engineering hub and wiki the Stem Player scene is built on.
- **[dot-Justin](https://github.com/dot-Justin)** - the [lines-thread archive](https://github.com/dot-Justin/TE-SP-1-lines-thread-archive) and the cited [SP-1 knowledgebase](https://github.com/dot-Justin/SP-1-knowledgebase-skill) that set the bar for honest, sourced documentation this list aims to live up to.
- **[Kevin Morrill (kmorrill)](https://github.com/kmorrill)** - the [xy-format](https://github.com/kmorrill/xy-format), [EP SysEx](https://github.com/kmorrill/ep-series-sysex), and [OP-Z SysEx](https://github.com/kmorrill/op-z-sysex) protocol work that opened up three device families.

...and every contributor named throughout the linked projects.

## Contributing

Found something missing or stale? See [CONTRIBUTING.md](CONTRIBUTING.md) - one-line entries, honest status, curate don't collect. Dead links are caught weekly by the [link-check workflow](.github/workflows/link-check.yml).

## License

To the extent possible under law, contributors have waived all copyright and related rights to this work under [CC0 1.0 Universal](LICENSE).

*Last reviewed: 2026-09-25.*
