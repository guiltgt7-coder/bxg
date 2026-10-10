# Mod journal

## 2026-10-10

The user instructed us to ignore their GitHub repository and create a new BONELAB + GTA V Enhanced mashup. No project existed. The interview established BONELAB as VR primary, a real GTA neighborhood as companion content, solo first, native physical weapons and grabbable props, plus moving pedestrians and cars. Do not re-interview these decisions.

Melty authenticated discovery succeeded. No existing user drafts/listings. Search found no mashup combining the two games. Read both game_info results and the `gta-x-assetto-corsa` example. Its anti-cheat-disabling launch argument violates current instructions and must not be copied. BONELAB's supported automatic loader is MelonLoader v0.7.3. GTA companion content should be read without launching or modifying GTA. No requirement for Script Hook V or GTA ASI loading is proposed.

Cloned universal-modder from its official repository at commit `550651675153070cce68066e07c3c8f95df86d08` under workspace/repos/universal-modder. Read its mod-any-game skill, relevant engine guides, mashup skill and route/evidence field notes. Toolkit knowledge has no BONELAB note. Its GTA passthrough example targets Legacy and Script Hook V, and is not evidence of Enhanced archive compatibility.

Initial toolkit KB commands failed because system Python 3.9 lacked PyYAML and did not meet the toolkit's >=3.10 requirement. Installed uv 0.13.0 from Astral's official installer and used the toolkit's bin/um launcher with uv. KB search then succeeded. `um scan --list` reports no Steam/Epic/Xbox installs. `um win ps` exits 1 because this is Linux, not Windows or WSL. No games, headset, GPU game session or remote PC bridge are exposed here.

Read official CodeWalker and MarrowSDK READMEs over HTTPS. CodeWalker documents RPF, YMAP and world LOD but its README does not prove Enhanced support. An attempted MarrowSDK LICENSE.md fetch returned 404: redistribution permissions remain unverified; do not bundle it without checking the actual license.

Chosen candidate route: content read in place into BONELAB through MelonLoader; real GTA map/model/texture/collision data must reach the runtime. This is a proposal, not a working importer. Unknown install versions and integration hooks are explicit unfinished sheet cells. No build is permitted until preflight is clean.

Next: continue with access to the user's Windows installations and headset; inspect only relevant game files; verify the Enhanced archive reader and a single real textured object with physical collision in BONELAB. Resolve technical cells before code generation/build. Expand to neighborhood/pedestrians/traffic afterward. If a concrete obstacle requires changing the user's design, explain it and obtain agreement first. Preserve all publishing gates and final approval.
