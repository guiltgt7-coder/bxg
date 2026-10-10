# BONELAB: Los Santos — working title

**Design and research only. No playable build exists yet.**

A solo VR sandbox inside the real BONELAB game, in a neighborhood loaded from the player's own Grand Theft Auto V Enhanced installation. Walk with BONELAB's VR body, grab and throw loose objects, and use BONELAB's physical weapons. Moving traffic and pedestrians are required for the first playable version.

## Confirmed design

- BONELAB is the primary game and owns the player, headset view, hands, movement and physical interactions.
- GTA V Enhanced is a required companion providing the actual neighborhood, streets and buildings. Preserve Enhanced; do not substitute GTA Legacy.
- The first version includes a neighborhood, rather than a single room or all of Los Santos.
- Solo first. No multiplayer server or player limit is implied.
- Traffic and pedestrians are required. Drivable vehicles have not been requested.
- Gameplay is in BONELAB's VR view. No extra gameplay window was requested.

## Proposed implementation, awaiting actual file inspection

Use a MelonLoader mod in BONELAB, with Melty automatically installing its supported loader. Melty supplies the GTA companion folder through a mod-specific environment variable. Read only the needed GTA files in place and construct meshes, materials and collision in BONELAB's memory. Do not export, cache, bundle or copy GTA content into BONELAB's installation. Do not patch or launch GTA or disable BattlEye. Native BONELAB interactions remain in BONELAB.

Actual archive support for Enhanced, model/material/collision conversion, BONELAB integration hooks and traffic/pedestrian behavior remain unverified. Do not describe these as implemented. CodeWalker's README documents GTA archive/map formats but does not establish compatibility with this user's Enhanced build. Determine usable, redistributable dependencies before implementation.

The JSON sheets are the source of truth. Each cell includes its value, verification flag and evidence. A verified design cell confirms a decision, not running code. Unverified cells block generation/build. Each final row must generate one code record after preflight succeeds.

## Required evidence before a release

1. Inspect both actual installs and record exact game versions, BONELAB Unity/IL2CPP details and working loader version.
2. Prove one actual Enhanced world object can be read in place, rendered with matching texture and collision, and touched in BONELAB VR. Then expand to the neighborhood.
3. Verify headset/controller input, native grabbing/throwing, weapons, pedestrians and traffic in the real game. Check VR performance and clean scene teardown.
4. Package only original code and licensed dependencies, record credits, and establish the user's content license and remix choice. These permissions remain undecided.
5. Run Melty inspect_package, validate_recipe and one_click_check on the exact archive and feature list. Test installation and launch through Melty.
6. Capture this exact build running in BONELAB. Finish the screenshot upload before publishing.
7. Show the release summary and obtain the user's final publish authorization. No draft or release has been created.

## Current access blocker

The current session runs in an Amazon Linux cloud workspace. The games on the user's Windows PC and the VR headset are not mounted or remotely controllable. Toolkit discovery reports no game installs; `um win ps` rejects this non-Windows/non-WSL host. Continue in a coding-agent session running on that Windows PC, or WSL on that same PC, with access to both installed games and the headset. The agent should locate the games and perform setup; do not ask the user to install technical dependencies manually.

Credentials are intentionally absent. Obtain a fresh Melty Publish prompt in the continuation session if needed; never put its token in project files.
