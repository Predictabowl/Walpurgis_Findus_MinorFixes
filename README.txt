Walpurgis - Minor Fixes
================================

- v1.1.0
This patch prevents monsters equipped with shields from being accidentally "auto-fragged" (instant-killed) by movement-inducing effects.
In the original configuration, the monster and its shield are two separate solid entities. When an effect pushes or moves the monster, their hitboxes can intersect, causing the engine to detect a collision between two solid objects and instantly kill the monster.

Changes:
- Modified monster/shield interaction to prevent intersection deaths when moved.
- Ensures movement effects (like knockback or gravity) don't cause unintended instant kills on shielded actors.

Known Limitations:
- Pushing a shielded monster directly into level geometry (walls, corners, etc.) will still result in an instant kill (e.g., when Using the Disc of Repulsion). This is a limitation of the engine's collision handling with multiple solid parts and is currently considered acceptable behavior.


- v1.0.0
When the ultimate weapon is assembled, Ultimate weapons pieces placed on map will change into a weapon upgrader item, but only if player doesn't have any upgrader item in its inventory. You can disable this behaviour simply by removing the include "SpawnersUltWepons_FI" from inside the DECORATE file

Installation:
-------------
This is a patch for the Walpurgis mod. It MUST be loaded AFTER the main Walpurgis files to function correctly.

In the original configuration, the monster and its shield are two separate solid entities. When an effect pushes or moves the monster, their hitboxes can intersect, causing the engine to detect a collision between two solid objects and instantly kill the monster.

Related Projects:
-----------------
- Findus Patch: https://github.com/Predictabowl/Walpurgis_Findus_Patch_repo
- Walpurgis Minor Fixes: https://github.com/Predictabowl/Walpurgis_Findus_MinorFixes
- Faithless Trilogy Compatibility: https://github.com/Predictabowl/Walpurgis_Findus_Faith_Tri_repo

