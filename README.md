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
- 🟢 [CircuitPython for SP-1](https://circuitpython.org/board/teenage_engineering_sp1) - Official CircuitPython build flashed from the bootloader, with an [Adafruit guide](https://learn.adafruit.com/hacking-the-teenage-engineering-sp-1); permanently erases stock firmware and all stored songs, so back up first.
- 🟢 [sp1-tape-looper](https://github.com/chattock/sp1-tape-looper) - Four-track tape-machine looper firmware, stereo with FX since v3, with a recovery bin and an [interactive guide](https://sp1-tape-looper.vercel.app); upgrading from v2 erases songs, so export first.
- 🟢 [Wakes](https://github.com/Worldwave/Wakes) - Beta firmware that makes the SP-1 a semimodular macro-synth from Mutable Instruments Plaits, Marbles and Yarns, with a full manual; the author warns stock firmware cannot be restored after flashing.
- 🟢 [Bonsai 8](https://github.com/AWD-tech/bonsai-8) - Experimental two-deck firmware that mixes eight stems from two songs, with a browser companion; tempo following still has pitch and transient artifacts.
- 🟢 [marisko](https://github.com/jackiscool123123121/marisko) - Actively released community firmware, loaded with its rome CLI, continuing [softmodded's original](https://github.com/softmodded/marisko); still work in progress.
- 🟢 [feldd](https://feldd.com) - Turns the SP-1 into a USB, Bluetooth and TRS MIDI controller; map the faders and buttons to any CC or note from the browser, with per-control channels for a mixer.
- 🟢 [SP-1 Remote](https://github.com/mortenwagner/sp1-remote) - Open-source, build-from-source firmware that turns the SP-1 into a four-fader, four-button MIDI controller over TRS and USB.
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
- 🟢 More SP-1 stem loaders: [rome](https://github.com/jackiscool123123121/rome) (marisko's flashing and stem CLI, with macOS, Windows and Android apps), [sp1-loader](https://github.com/sh4tteredd/sp1-loader) (Python CLI and GUI), [SP1 Loader for Android](https://github.com/JewMoney10/sp1-loader) (native USB app where Chrome's Web Serial loader fails).

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
- 🟢 [tp7](https://github.com/totocaster/tp7) - Scriptable Rust macOS CLI that flips the TP-7 into MTP mode and lists, pulls, pushes and deletes files without Field Kit.
- 🟢 [tp-7-mtp](https://github.com/sparkyfen/tp-7-mtp) - The Linux route to TP-7 files without Field Kit: SysEx MTP switch, tray app, APT repo, and reverse-engineering notes.
- 🟢 [tp7 (Linux TUI)](https://github.com/plue17/tp7) - Terminal app that imports, organizes and plays TP-7 voice memos on Linux over the GNOME gvfs MTP mount.
- 🟢 [TP-7-VoiceSync](https://github.com/armynante/TP-7-VoiceSync) - macOS menu bar app that auto-syncs, transcribes and files TP-7 memos to Apple Notes ([active fork](https://github.com/cwill747/TP-7-VoiceSync) adds Parakeet, diarization and Notion).
- 🟢 [wavesync](https://github.com/pixelate/wavesync) - Ruby CLI that converts a music library to TP-7 spec and syncs it to the device over MTP.
- 🟢 [tp7-station](https://github.com/krystalmaria/tp7-station) - Signed macOS app that auto-syncs the TP-7, transcribes memos on-device, and writes edited cue points back to the recorder.
- 🟢 More TP-7 memo sync and control apps: [TP-7 Manager](https://github.com/joshualexanderl/TP-7-Manager), [TP7 Vibe Deck](https://github.com/PacoZhou1/tp7-vibe-deck) (TP-7 as a Mac control surface), [tp7sync](https://github.com/Aias/tp-7) (diarized transcripts plus a gesture-driven meeting-capture menu bar app).
- 🟡 [tp7-util](https://github.com/mellson/tp7-util) - macOS app to split and combine TP-7 multitrack polyWAV stems for DAW workflows.

### Teardown, flashing & recovery

- 🟢 [TP-7 Disassembly Tools](https://www.printables.com/model/1478390-teenage-engineering-tp-7-disassembly-tools) - 3D-printable non-standard tools to open a TP-7, though the author warns disassembly likely bricks it.

### Community

- 🟢 [Teenage Engineering TP-7 thread (lines)](https://llllllll.co/t/teenage-engineering-tp-7/63256) - The main community hub for TP-7 workflows, tips and teardown chatter.

## OP-XY

### Reverse engineering & docs

- 🟢 [kmorrill/xy-format](https://github.com/kmorrill/xy-format) - Byte-exact decode of the OP-XY .xy project format with Python tools to inspect, edit, and generate projects, the anchor reference for the scene.
- 🟢 [OP-XY MIDI CC sheet](https://docs.google.com/spreadsheets/d/1zRCaETkKXG4sMAbXxMcYvS4RCCAOrMtmAxHE4lVH8CU) - Community map of OP-XY MIDI CCs per track type, including undocumented ones like the CC86 preset picker.

### Tools & software

- 🟢 [kmorrill/op-xy-vibing](https://github.com/kmorrill/op-xy-vibing) - AI-assisted JSON loop editor that plays to OP-XY over USB-C MIDI and exports presets.
- 🟢 [XY Workbench](https://tonicmidi.com) - Free browser editor built on xy-format that opens, edits, and re-exports .xy projects in the browser.
- 🟢 [XY Buddy](https://xybuddy.xyz) - Web utility that turns MIDI files into OP-XY projects and exports .xy patterns back to MIDI.
- 🟢 [OP-XY Agent](https://github.com/NeoVand/op-xy-agent) - Browser replica of the OP-XY with an AI agent that answers from the manual and programs the device over USB MIDI.
- 🟢 [sixthlaw/opxy-multisampler-preset-builder](https://github.com/sixthlaw/opxy-multisampler-preset-builder) - Browser tool to drag-drop audio into OP-XY multisampler preset folders with automatic pitch detection.
- 🟢 [OP-XY Drum Utility](https://drumutility.yuugo.xyz) - Browser take on TE's Drum Utility that builds OP-XY kits with per-slot trim, reverse, bit depth and rate.
- 🟢 [OP-XY-Sample-Extractor](https://github.com/buba447/OP-XY-Sample-Extractor) - Python scripts that read a .xy project and back up its user samples over MTP; factory samples are excluded.
- 🟢 [ConvertWithMoss](https://github.com/git-moss/ConvertWithMoss) - Converts multisamples from Kontakt, SFZ, SF2, EXS24, Akai and dozens more into OP-XY preset folders, warning about samples over the device's length limit.
- 🟢 OP-XY preset/sample format converters: [SF2 in](https://github.com/charlesvestal/sf2-to-opxy), [SFZ out](https://github.com/legsmechanical/opxy-to-sfz), [DX7 SYSEX](https://github.com/cfurrow7/dx7-opxy), [Elektron .elmulti](https://github.com/cfurrow7/opxy-converter), [NI Maschine](https://github.com/DimaDake/maschine-multisample-to-op-xy-converter), [Logic/GarageBand kits](https://github.com/inrainbws/logic_pro_drums_for_opxy), [REX/sliced loops](https://github.com/g-lok/chirashi).
- 🟢 More OP-XY preset generators: [PolySampler](https://github.com/Calvin-Zikakis/polysampler) (VST3/CLAP plugin that auto-multisamples any MIDI instrument, build from source), [MI Multisampler](https://cfurrow7.github.io/rings-multisampler) (synthesizes presets from modal, Karplus-Strong and FM engines).
- 🟢 [stembounce](https://github.com/om3opr/stembounce) - Browser tool that MIDI-solos each OP-XY track and records per-track WAV stems, for firmware before 1.2's native multichannel USB audio.
- 🟢 [OPXY.APP](https://opxy.app) - Browser tool that renames and relinks OP-XY samples across every project, flags truncated filenames, and batch-downsamples to free space.
- 🟢 [vjxy](https://vjxy.app) - MIDI-driven live visual instrument for the OP-XY: trigger video clips from notes and steer FX with CC.
- 🟢 [opxy-deck](https://github.com/kazuochi/opxy-deck) - Turns the OP-XY into a macro deck for AI coding agents, with a full map of its controller-mode MIDI output.
- 🟢 [playOPXY](https://github.com/cfurrow7/midi-playbox) - Monome norns jukebox that auto-routes MIDI-file parts to OP-XY default tracks over USB for instant playback.
- 🟡 [OP-XY CTLR](https://pkpatches.gumroad.com/l/op-xyctlr) - Paid Max for Live device that edits OP-XY synth, filter, envelope, LFO and FX parameters from Ableton, with stored presets.
- 🟡 [OP-PatchStudio](https://op-patch.studio) - Free browser app for OP-XY drum and multisample presets, with OP-1 drum-preset import.
- 🟡 [buba447/OPXY-Multisample-Tool](https://github.com/buba447/OPXY-Multisample-Tool) - Python scripts to record and pack WAV/AIFF samples into OP-XY multisample presets.
- 🟡 [buba447 OP-XY Drum & Multisample Patch Generator](https://buba447.github.io/opxy-drum-tool) - Hosted web generator that builds OP-XY drum kits and multisample patches from audio files.
- 🟡 More OP-XY drum kit builders: [op-xy-drum-builder](https://github.com/niekert/op-xy-drum-builder) (web app for drum racks from your own audio), [op-xy-drum-preset-builder](https://github.com/discepoli/op-xy-drum-preset-builder) (presets from a list of sample files).

## OP-Z

### Reverse engineering & docs

- 🟢 [OP-Z SysEx](https://github.com/kmorrill/op-z-sysex) - Device-proven docs for OP-Z SysEx, StateSync, and file transfer, plus Python tools for guarded project and sample writes.
- 🟢 [libopz](https://github.com/patriciogonzalezvivo/libopz) - Unofficial C++ library to parse .opz project files and talk to the OP-Z over MIDI/SysEx.
- 🟢 [opz-firmware-notes](https://github.com/ioma8/opz-firmware-notes) - Ongoing OP-Z firmware research notes: factory plug tables, settings file formats, and a documented NAND-brick warning.
- 🟡 [z-po-project](https://github.com/lrk/z-po-project) - Reverse-engineering wiki documenting OP-Z internals, the original community protocol reference.
- 🟡 [OPZ.js](https://github.com/nbw/opz) - JavaScript library that decodes OP-Z sequencer MIDI in the browser for creative-coding visuals and games.

### Tools & software

- 🟢 [vcvopxyz](https://github.com/un1tz3r0/vcvopxyz) - VCV Rack plugin recreating the OP-Z sequencer and engines, importing and exporting real OP-Z projects and kits, with CV breakouts.
- 🟢 [OP-Z Studio](https://agolg.github.io/opz-studio) - Browser editor that reads and writes OP-Z patterns over USB SysEx, backing up first and verifying after (French UI).
- 🟢 [OP-Z Manager](https://github.com/dougal441/opztrackmanager) - macOS librarian that names, archives, and safely restores or swaps OP-Z project slots beyond the 10-slot limit.
- 🟢 [Teenage OP-Z Editor and Controller](https://teenage-op-z-edtior.jimdofree.com) - Paid VST/AU and standalone editor showing all eight OP-Z tracks' parameters on one screen, with XY modulation.
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

- 🟢 [OP-Z-Replacement-Battery](https://github.com/abux77/OP-Z-Replacement-Battery) - Open frame and PCB that fit a standard PH2.0 LiPo, replacing the discontinued official OP-Z battery.
- 🟡 [OP-Z-Cube](https://github.com/MateSteinforth/OP-Z-Cube) - Arduino-driven LED light object that reacts live to the OP-Z.

### Community

- 🟢 [Videolab Resources](https://github.com/Videolab-Creators-Group/Videolab-Resources) - The Videolab Creators Discord's starter hub for videopaks, with a Unity template, deep docs, and shader tools.

## OP-1 / OP-1 field

### Custom firmware & OS

The 2026 custom-firmware wave below targets the **original OP-1 on OS 246** only; OP-1 field firmware is encrypted and has no public custom firmware. These are unofficial: they can brick the unit or leave saved sounds that stock firmware can't load, so back up first and follow each project's recovery steps.

- 🟢 [op1r](https://github.com/pcppcp/op1r) - The first full custom firmware for the original OP-1: new engines, sequencers, sample editor and plugins, patched in-browser ([source and SDK](https://github.com/pcppcp/op1r-src)).
- 🟢 [Hundekraft OP-1 Firmware Workshop](https://hundekraft.github.io/op1-workshop) - Browser configurator that builds custom original OP-1 firmware from picked synths, effects and plugins, then updates over USB MIDI.
- 🟢 [maiko OS](https://maikopruett.com/op-1) - Free custom OS for the original OP-1 adding tape undo/redo, four tapes, new effects, and a fix for TE's flash bad-block bug; heads-up: it ships as a ready-to-flash file containing TE's firmware, with no source published.
- 🟢 [op1-sdk](https://github.com/BertBrandstifter/op1-sdk) - MIT SDK and simulator for writing original OP-1 engines, effects and sequencers in C, with a six-engine op1plus image whose STATION 1 samples are proprietary KORG content, not MIT.
- 🟢 More original OP-1 mods: [Opus](https://opus-op1.pages.dev) (browser patcher: dimension and amp engines, scales, tape undo, clean back to stock), [op1-overdub](https://github.com/wsbuck/op1-overdub) (va, wavetable and grain engines, HOLD and CHORD modes), [Musica Obscura](https://github.com/ultralazr/op1-musica-obscura) (six history-of-sound modules, now shipping in op1r), [Note Quantization](https://github.com/stfj/OP-1-Note-Quantization-PublicGit) (scale quantize on shift+2, the wave's first patch).
- 🟢 [op1hacks](https://github.com/op1hacks) - Primary GitHub org for OP-1 firmware hacking: repacker, docs, firmware archives, and preset tools.
- 🟢 [op1repacker](https://github.com/op1hacks/op1repacker) - Unpacks, modifies, and repacks OP-1 firmware to unlock hidden iter synth, filter, and custom graphics mods.
- 🟢 [op1REpackerGUI](https://github.com/epixjava/op1REpackerGUI) - Desktop GUI front-end for op1repacker, making OP-1 firmware mods accessible without the CLI.
- 🟡 [op1-fw-archive](https://github.com/op1hacks/op1-fw-archive) - Unofficial mirror of (almost) all original OP-1 firmware versions for downgrade and research; prefer TE's official downloads where available.
- 🟡 [op1-glitter](https://github.com/Nanobot567/op1-glitter) - Custom color themes for the original OP-1, patched into its firmware from a JSON file via op1repacker.
- 🟡 [op1-field-fw-archive](https://github.com/op1hacks/op1-field-fw-archive) - Unofficial mirror of OP-1 field firmware releases with changelog notes, useful for downgrade and study; prefer TE's official downloads.

### Reverse engineering & docs

- 🟢 [te-op1](https://github.com/jstnfst/te-op1) - OP-1 field preset-format reference and community patch library with a browser editor, plus the mondo C toolkit for patches and whole-device backup.
- 🟢 [op1-mod-registry](https://github.com/LizardMan245/op1-mod-registry) - Shared list of the engine, effect and LFO names each OP-1 246 mod claims, so mods don't clash or crash stock.
- 🟢 [OP-1 & OP-1 Field Tips](https://brigleb.github.io/op1-tips) - Cleaned-up, link-checked edition of the op-forums tips thread with Field notes; see also the older [op1tips digest](https://github.com/ratbag98/op1tips).
- 🟡 [ghidra-blackfin](https://github.com/sualk/ghidra-blackfin) - Blackfin CPU support for Ghidra, the disassembly groundwork the 2026 OP-1 mods credit; see also [op1-decryptor](https://github.com/sualk/op1-decryptor).
- 🟡 [op1-docs](https://github.com/sualk/op1-docs) - Documentation and reverse-engineering research on OP-1 firmware and hardware internals.
- 🟡 [sowbug/op-1-tools](https://github.com/sowbug/op-1-tools) - Reverse-engineering research and tooling on the OP-1's file formats and internals.

### Tools & software

- 🟢 [op1.fun](https://op1.fun) - Community hub to download and share 12,500+ patches, with an in-browser drum builder and macOS sync app.
- 🟢 [op1emu](https://github.com/op1emu/op1emu) - Original OP-1 emulator on a Blackfin JIT that boots firmware 246, so mod builds get tested before flashing.
- 🟢 [op1-lfo-hero](https://github.com/andrewralon/op1-lfo-hero) - Sends beat-synced LFO automation to the OP-1 field, TX-6 and TP-7 over USB-C or BLE MIDI, as desktop and iOS apps.
- 🟢 [op-bridge](https://github.com/CrabbTech/op-bridge) - MCP server that lets an AI play the OP-1 field over USB MIDI, then records and checks what it heard.
- 🟢 [Sync for OP-1](https://github.com/UndeRus/SyncForOP1_releases) - Closed-source Android app that backs up and restores an original OP-1 over USB, with a drum-kit browser and tape player.
- 🟢 [op1microtonal](https://github.com/robinmeier/op1microtonal) - Browser tool that bakes Scala microtonal scales into OP-1 drum patches for exact tuning beyond semitones.
- 🟢 More ways to use an OP-1 as a controller: [Zynthian driver](https://wiki.zynthian.org/index.php/Teenage_Engineering_OP-1) (plug-and-play in the open Zynthian synth platform, OS 246), [FL Studio script](https://github.com/ryrun/FL-OP1-controller-script) (transport and window keys).
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

- 🟢 [OP-1 te-boot recovery over JTAG](https://github.com/jheidecker/OP-1-te-boot-recovery-over-JTAG) - Documented repair of an original OP-1 whose te-boot no longer starts; its boot-NAND writes can brick the unit, so keep verified backups.
- 🟡 [iFixit OP-1 repair guides](https://www.ifixit.com/Device/Teenage_Engineering_OP-1) - Twelve step-by-step teardown/repair guides: battery, display, keyboard, connector board, flex cable.
- 🟡 [op1dumps](https://github.com/Tolsi/op1dumps) - Unofficial flash/OTP dumps, schematic, and bootloader for replacing a dead OP-1 processor or flash chip.

### Community

- 🟢 [Custom firmware on the OP-1 (op-forums)](https://op-forums.com/t/custom-firmware-on-the-op-1/4283) - The 1,300+ post thread where op1r, Hundekraft, Opus and the other OP-1 mods are released, tested and debugged.

## EP series (K.O. II, EP-1320, EP-40, EP-136)

### Custom firmware & OS

- 🟢 [ep-unity](https://github.com/seajaysec/ep-unity) - Browser WebMIDI tool that cross-flashes between K.O. II and EP-40 Riddim firmware by rewriting four SKU bytes, with backups; unsupported and can brick.

### Reverse engineering & docs

- 🟢 [EP SysEx](https://github.com/kmorrill/ep-series-sysex) - Capture-verified docs for the shared EP-133/EP-40 SysEx protocol and project format, with a JSON project compiler and hardware tools.
- 🟢 [EP-133 cheat sheet](https://ep133.joeyh.org) - Searchable, printable one-page reference for K.O. II button combos, system settings, and modes.
- 🟢 [Riddim + Ting guide](https://ourtinyapps.github.io/riddim-n-ting) - Interactive EP-40 and EP-2350 button map: tap a combo on the drawn panel to see what it does.
- 🟢 [EP-136 MIDI CC map](https://gist.github.com/GOROman/9d47019539823b119c663e1bb1034445) - Device-tested map of the K.O. Sidekick's MIDI CCs, channels, and relative encoder format for building controller mappings.
- 🟡 [KOII-tips-and-tricks](https://github.com/vebam/KOII-tips-and-tricks) - Community guide of K.O. II tips distilled from Elektronauts threads, a full-history mirror of Neil Baldwin's deleted original.
- 🟡 [ep_133_sysex_thingy](https://github.com/garrettjwilke/ep_133_sysex_thingy) - Reverse-engineered SysEx command library and docs to manage K.O. II samples without the official tool.

### Tools & software

- 🟢 [ep133-export-to-daw](https://github.com/phones24/ep133-export-to-daw) - Reverse-engineered WebMIDI tool exporting full K.O. II projects to Ableton, REAPER, DAWproject, and MIDI; hosted at ep133-to-daw.cc.
- 🟢 [ep133-krate](https://github.com/icherniukh/ep133-krate) - CLI and terminal-UI sample manager built on a reverse-engineered SysEx protocol.
- 🟢 [ep133-ppak](https://github.com/ZacharySBrown/ep133-ppak) - Python library and CLI to write valid .ppak sample-mode and song-mode project files from JSON.
- 🟢 [StemForge](https://github.com/ZacharySBrown/stemforge) - Demucs stem-split and bar-slicing pipeline that turns any track into a hardware-ready K.O. II .ppak kit, with Ableton integration.
- 🟢 [EP Toolkit](https://eptoolkit.ep133-to-daw.cc) - Native EP-133/1320/40 app: project export to DAWs, full sample management, CLAP processing, and device backups.
- 🟢 [AudioBatchConverter](https://github.com/JanSchulten/AudioBatchConverter) - Batch-prepares audio samples for the K.O. II and exports sample chains for the PO-33.
- 🟢 [EP-PatchStudio](https://squarewave.studio/ep-patchstudio) - EP-133/1320/40 app for desktop, iOS and Android: free sample and EP-40 multisample editor, paid Pro for device management, backups and auto-sampling.
- 🟢 [Best Friend](https://epbf.app) - Companion app for EP-133, EP-40, and EP-1320 on iPhone, iPad, Mac, and Android that shows scenes and bounces real per-pad stems from the hardware.
- 🟢 [EP-REC field recorder](https://github.com/hirbehozo/ep-rec-field-recorder) - Android browser app that records synced audio and MIDI takes from the K.O. Sidekick and K.O. II over USB.
- 🟢 [1a2n-sidekick](https://github.com/abuzucom/1a2n-sidekick) - Traktor Pro 4 mapping that turns the K.O. Sidekick into a four-deck DJ controller with loops, EQ, and jog.
- 🟢 More EP tools: [ko2-io](https://github.com/trusch/ko2-io) (Linux CLI and FUSE mount), [PunchKit](https://punchkit.dev) (iPhone, iPad and Mac kit builder, on-device stem splitter and backups), [EP Audio Editor](https://www.mediachance.com/epaudioeditor) (Windows, EP-40 multisamples), [KO II Sampler DAW](https://github.com/generalgroovy/ko) (Windows sample editor, MIDI recorder and scene arranger), [K.O. Tool](https://zatumanen.github.io/Ko-tool) (Russian-language web app that halves sample memory via 2x speed and pitch compensation).
- 🟢 [ko-bridge](https://github.com/CrabbTech/ko-bridge) - MCP server for the EP-133 that writes samples and projects byte-verified and records OS 2.5 USB audio to grade timing.
- 🟢 More K.O. II MCP servers: [ep133-mcp](https://github.com/wil-gerard/ep133-mcp) (samples, kits, .ppak projects), [kobox](https://github.com/yangyue1974/kobox) (pads and scales), [koii-controller](https://github.com/xhiew/koii-controller) (native Swift, macOS).
- 🟡 [mcp-koii](https://github.com/benjaminr/mcp-koii) - MCP server controlling the K.O. II over MIDI so an LLM can play notes and patterns.
- 🟡 [Cornerman for K.O. II](https://apps.apple.com/us/app/cornerman-for-k-o-ii/id6499280264) - iOS app that backs up the K.O. II offline, without TE's web tool.
- 🔴 [ep_133_sample_tool](https://github.com/garrettjwilke/ep_133_sample_tool) - Offline fork of the EP sample tool adding projects-only backup and raw SysEx debugging.

## EP-2350 Ting FX

### Custom firmware & OS

- 🟢 [CircuitPython for EP-2350](https://circuitpython.org/board/teenage_engineering_ep2350) - Official CircuitPython build that replaces the Ting's stock MicroPython firmware, reversible by flashing TE's firmware back.
- 🟢 [ep-2350-usb-mic](https://github.com/JR-One-Yard/ep-2350-usb-mic) - CircuitPython firmware that makes the Ting a class-compliant USB microphone for a Mac or USB-C iPhone, with stock backup.

### Reverse engineering & docs

- 🟢 [open-ting](https://github.com/au42/open-ting) - MicroPython and binary dumps, docs, and drag-and-drop examples for advanced features out of the box.

### Tools & software

- 🟢 [FX-USB](https://github.com/danilosierrac/fx-usb) - Early Apple-silicon Mac app that makes the Ting a USB microphone with its effects intact, using a RAM-only reader; nothing flashed.
- 🟢 [tink-agent](https://github.com/tajchert/tink-agent) - macOS menu-bar app that turns the Ting into push-to-talk plus eight button macros for AI coding agents, signaled by tones over line-out.
- 🟢 [Ting Preset Editor](https://ting.supervisedmusic.com) - Web preset editor with drag-and-drop effect chains, emulated audio preview, and live Web Serial sync to the Ting.
- 🟢 [EP-2350 config editor](https://tadao314.github.io/ep2350-config-editor) - Offline single-file editor for the Ting's config.json that enforces effect ranges and remaps modulation when you reorder chains.
- 🟢 More Ting push-to-talk tools: [tingle](https://github.com/tutorintelligence/tingle), [ting-bridge](https://github.com/l7073a/ting-bridge), [fx-mic-claude](https://github.com/migueldelag/fx-mic-claude), [reasoning-ting](https://github.com/jof/reasoning-ting), [FX Talk](https://github.com/bjg4/fx-talk), [tingtype](https://github.com/micthiesen/tingtype) (macOS and Linux, tap/hold/double-tap gestures).
- 🟢 More Ting config tools: [fx-mic-tool](https://github.com/oxo-yuta/fx-mic-tool) (validator and live audio preview), [Adafruit config tool](https://github.com/adafruit/TE_EP2350_Config_Tool) (for the CircuitPython demo), [Mic Gnome](https://micgnome.pages.dev) (boot-safe validator plus a 38-preset library).

### Teardown, flashing & recovery

- 🟢 [EP-2350 teardown (informal)](https://informalcc.notion.site/Teenage-Engineering-Ting-FX-EP-2350-teardown-31a0865a6819806198e0db6eb796b304) - Photo teardown of the Ting by a mechanical engineer, with a companion video.
- 🟢 [Hacking the EP-2350 Ting (Adafruit)](https://learn.adafruit.com/hacking-the-teenage-engineering-ep-2350-ting) - Teardown, reverse-engineered pinout, and step-by-step CircuitPython flashing, plus a demo approximating the stock firmware.

## Pocket Operators

### Custom firmware & OS

- 🟡 [Hanz Tech PO MIDI Adapter V3](https://github.com/Hanz-Tech/midi-adapter-v3-software) - Adapter firmware taking USB/DIN MIDI in and pressing PO buttons via GPIO.

### Reverse engineering & docs

- 🟢 [libpo32](https://github.com/ericlewis/libpo32) - Portable C99 reimplementation of the PO-32 Tonic's acoustic modem and drum voice, so software can build and send patches and patterns.
- 🟢 [po-backup-decode](https://github.com/danielpradilla/po-backup-decode) - Python decoder for PO-33 transfer WAVs that pulls out samples, patterns and BPM, with the modem protocol documented.

### Tools & software

- 🟢 [PO-PatchStudio](https://squarewave.studio/po-patchstudio) - Free desktop and mobile app built on libpo32 that designs PO-32 Tonic sounds and patterns and sends them acoustically.
- 🟢 [POTool](https://github.com/andreaskinga-lgtm/POTool) - Desktop 16-pad editor that trims, slices, and merges samples into one WAV for loading into a PO-33.
- 🟢 [DrumMachinePO](https://github.com/signfang/DrumMachinePO) - Sideloadable Playdate 16-step sequencer with pattern chaining that sends sync pulses to drive Pocket Operators.
- 🟢 [po-12](https://github.com/ulnd/po-12) - Installable browser emulation of the PO-12 rhythm for learning the sequencer without the hardware.
- 🟢 [Pocket Operations Manual](https://udeudeude.github.io/Pocket-Operations-Manual) - Phone-friendly PO-35 Speak emulator and interactive tutor with a working sequencer, voices, effects, and pattern chaining.
- 🟡 [po-33](https://github.com/rileyjshaw/po-33) - Clean browser drag-and-drop loader that records sample banks into the PO-33 K.O.
- 🟡 [PocketSync](https://github.com/chr15m/PocketSync) - Phone and web app that outputs the Pocket Operator sync pulse, no extra hardware needed.
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
- 🟢 [OD-11 Web App](https://github.com/paolocamerin/od11-webapp) - Zero-dependency local browser app controlling OD-11 volume and playback directly over its WebSocket API.
- 🟢 [ortho-remote-mac](https://github.com/araa47/ortho-remote-mac) - macOS tool mapping the Ortho Remote knob to volume, play/pause, and Spotify navigation.
- 🟢 [ha-orthoplay](https://github.com/vibrog/ha-orthoplay) - Home Assistant integration giving the OD-11 local control of volume, sources, and playback over its WebSocket API.

## Choir

### Reverse engineering & docs

- 🟡 [Choirama](https://github.com/jetztgradnet/Choirama) - Community findings on the Choir dolls, from voice ranges and BLE MIDI pairing to the consonant and vowel CCs that make them sing.

### Tools & software

- 🟢 [Choir Arranger](https://github.com/dderuntz/choir-editor) - Notarized macOS app with a piano roll and text-to-song composer for the Choir dolls, plus OP-XY project export.
- 🟢 [talking-with-a-choir](https://github.com/tiny-factories/talking-with-a-choir) - Mac app that turns typed text into consonant and vowel MIDI CCs so the Choir dolls sing your words.

## Cross-device tools

### Tools & software

- 🟢 [DigiChain](https://github.com/brian3kb/digichain) - Builds and splits sample chains and kits for OP-1 Field, OP-Z, and OP-XY in the browser.
- 🟢 [OP-1Z-Sample-Manager](https://github.com/romangarms/OP-1Z-Sample-Manager) - Cross-platform desktop app for managing OP-Z and OP-1 samples.
- 🟢 [TEKit](https://github.com/ericlewis/TEKit) - Swift package controlling TE devices (OP-Z/TP-7/OB-4/OD-11) over BLE, USB, and WebSocket.
- 🟢 [Swift-TE](https://github.com/matthewjschultz/swift-te) - Dependency-free Swift package that writes OP-1/OP-Z patches and OP-XY drum and multisample presets for native Apple tools.
- 🟢 [field-remote](https://github.com/jwamin/field-remote) - SwiftUI iOS BLE MIDI remote for TE field gear, with control panels for TX-6 and TP-7.
- 🟢 [MTVP](https://mtvp.app) - Free iOS and Android app that plays video locked to your OP synths' MIDI transport and timecode.
- 🟢 [Studio Field](https://studiofield.app) - Paid companion that backs up and transfers content across TE devices, including OP-1 field and OP-XY straight from an iPhone.
- 🟢 [Pocket Operations](https://5of12.github.io/PocketOperations) - Browser port of the Pocket Operations drum-pattern book that records patterns straight into an OP-XY or OP-1 field over Web MIDI.
- 🟢 More sample prep and kit builders: [TRKLS](https://trkls.net) (OP-1, OP-1 field, OP-Z, EP-133), [Earthwire](https://earthwire.space) (OP-1 field kits from Freesound and Xeno-canto), [Sample Trimmer](https://sampletrimmer.com) (offline batch trim and shrink to fit K.O. II, OP-1 and PO memory).
- 🟢 [op-patch-util](https://github.com/AlexCharlton/op-patch-util) - Rust CLI to create and modify OP-1 and OP-Z drum patches, pitch, and metadata.
- 🟡 [teoperator](https://github.com/schollz/teoperator) - Turns any audio file into OP-1 and OP-Z drum and synth patches, with a hosted version.
- 🟡 [OP_Manager](https://github.com/adwuard/OP_Manager) - Raspberry Pi Zero handheld file manager for on-the-go backup and upload of OP-1/OP-Z patches.
- 🟡 [mezmer](https://github.com/idroz/mezmer-app) - Live sound visualizer that works with both OP-Z and OP-XY.

### Hardware mods

- 🟢 [TEcases](https://tecases.com) - Handmade protective cases sold for OP-1 field, OP-XY, EP-series, TP-7, TX-6, CM-15, Pocket Operators, and OB-4.

### Teardown, flashing & recovery

- 🟢 [dl-op-firmware-archive](https://github.com/workeffortwaste/dl-op-firmware-archive) - Script that fetches and checksums older OP-1 field, OP-XY, TX-6 and TP-7 firmware from TE's own URLs via the Internet Archive; unofficial, prefer TE's current downloads.

### Community

- 🟢 [op-forums.com](https://op-forums.com) - The primary active TE community forum and the hub where most firmware and tool research starts.

## Credits & inspiration

This directory exists because a few people did the hard reverse engineering and documented it carefully. Particular thanks to:

- **[TimK (timknapen)](https://github.com/timknapen)** - the [SP-1-dev](https://github.com/timknapen/SP-1-dev) hardware reverse-engineering hub and wiki the Stem Player scene is built on.
- **[dot-Justin](https://github.com/dot-Justin)** - the [lines-thread archive](https://github.com/dot-Justin/TE-SP-1-lines-thread-archive) and the cited [SP-1 knowledgebase](https://github.com/dot-Justin/SP-1-knowledgebase-skill) that set the bar for honest, sourced documentation this list aims to live up to.
- **[Kevin Morrill (kmorrill)](https://github.com/kmorrill)** - the [xy-format](https://github.com/kmorrill/xy-format), [EP SysEx](https://github.com/kmorrill/ep-series-sysex), and [OP-Z SysEx](https://github.com/kmorrill/op-z-sysex) protocol work that opened up three device families.
- **[pcppcp](https://github.com/pcppcp)** - [op1r](https://github.com/pcppcp/op1r) and its open plugin SDK, which reopened the original OP-1 to custom firmware in 2026.

...and every contributor named throughout the linked projects.

## Contributing

Found something missing or stale? See [CONTRIBUTING.md](CONTRIBUTING.md) - one-line entries, honest status, curate don't collect. Dead links are caught weekly by the [link-check workflow](.github/workflows/link-check.yml).

## License

To the extent possible under law, contributors have waived all copyright and related rights to this work under [CC0 1.0 Universal](LICENSE).

*Last reviewed: 2026-10-20.*
