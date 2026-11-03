# Credits

Dominion Fall is built almost entirely in code: geometry, shaders, sound
and music are generated at runtime. The exceptions are the photo-scanned
assets below.

## Poly Haven (CC0 1.0)

All of these come from [Poly Haven](https://polyhaven.com) and are released
under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/): no
attribution is required, and they are credited here anyway. They live in
`assets/polyhaven/` and were fetched with `tools/fetch_polyhaven.py`.

### Textures

| Asset | Resolution | Used for | Source |
|---|---|---|---|
| cliff_side | 2k (1k on the web) | Cliff and rock faces (terrain, rocks, spires) | https://polyhaven.com/a/cliff_side |
| dark_rock | 2k (1k on the web) | Darker rock variant | https://polyhaven.com/a/dark_rock |
| mud_cracked_dry_riverbed_002 | 2k (1k on the web) | Salt crust on the valley floor (bleached) | https://polyhaven.com/a/mud_cracked_dry_riverbed_002 |
| dry_ground_rocks | 2k (1k on the web) | Stony dry ground | https://polyhaven.com/a/dry_ground_rocks |
| grass_ground | 1k | Ground under the dry grass | https://polyhaven.com/a/grass_ground |
| road_damaged | 1k | The old Meridian road | https://polyhaven.com/a/road_damaged |
| concrete_layers_02 | 1k | Station ruins and walls | https://polyhaven.com/a/concrete_layers_02 |

| hessian_380 | 1k | Ash's mantle and hood, the pack | https://polyhaven.com/a/hessian_380 |
| poly_wool_herringbone | 1k | Ash's coat | https://polyhaven.com/a/poly_wool_herringbone |
| rough_linen | 1k | Ash's boot wraps and face wrap | https://polyhaven.com/a/rough_linen |
| fabric_leather_02 | 1k | Ash's gloves, boots and belt | https://polyhaven.com/a/fabric_leather_02 |
| denim_fabric_06 | 1k | Ash's trousers and inner layer | https://polyhaven.com/a/denim_fabric_06 |
| knitted_fleece | 1k | Ash's scarf | https://polyhaven.com/a/knitted_fleece |
| metal_plate_02 | 1k | The Pulse Rifle (worn gunmetal) and Ash's gear | https://polyhaven.com/a/metal_plate_02 |

### Models

| Asset | Textures | Used for | Source |
|---|---|---|---|
| namaqualand_cliff_01 | 1k | Cliff outcrops | https://polyhaven.com/a/namaqualand_cliff_01 |
| namaqualand_cliff_02 | 1k | Cliff outcrops | https://polyhaven.com/a/namaqualand_cliff_02 |
| mountainside | 1k | Cliff outcrops | https://polyhaven.com/a/mountainside |
| rock_face_01 | 1k | Boulders, outcrops | https://polyhaven.com/a/rock_face_01 |
| rock_face_02 | 1k | Boulders | https://polyhaven.com/a/rock_face_02 |
| rock_07 | 1k | Stones (scaled up) | https://polyhaven.com/a/rock_07 |
| rock_09 | 1k | Stones | https://polyhaven.com/a/rock_09 |
| namaqualand_boulder_03 | 1k | Boulders | https://polyhaven.com/a/namaqualand_boulder_03 |
| namaqualand_boulder_05 | 1k | Boulders | https://polyhaven.com/a/namaqualand_boulder_05 |
| dead_quiver_trunk | 1k | Dead trees | https://polyhaven.com/a/dead_quiver_trunk |
| dead_tree_trunk_02 | 1k | Fallen logs | https://polyhaven.com/a/dead_tree_trunk_02 |
| wild_rooibos_bush | 1k | Dry shrubs | https://polyhaven.com/a/wild_rooibos_bush |
| dry_branches_medium_01 | 1k | Dry branches | https://polyhaven.com/a/dry_branches_medium_01 |

### HDRI

| Asset | Resolution | Used for | Source |
|---|---|---|---|
| kloppenheim_01_puresky | 2k | The photographed base of the dusk sky | https://polyhaven.com/a/kloppenheim_01_puresky |

## Copernicus DEM (terrain shapes)

The shapes of the far mountain ranges come from the Copernicus GLO-30
Digital Elevation Model around the Salar de Atacama (22–25° S, 67–70° W),
read from the public copy on AWS (https://registry.opendata.aws/copernicus-dem/,
bucket `copernicus-dem-30m`, eu-central-1) and baked by `tools/bake_relief.py`
into `assets/terrain/atacama_relief.png`, a 512 × 512 relief map. The game
turns, rescales and exaggerates it; no real place is named or recreated.

> Produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus
> Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European
> Union and ESA; all rights reserved.

The Copernicus DEM GLO-30 is distributed free of charge, for any use
including commercial, under the Copernicus DEM licence
(https://spacedata.copernicus.eu/documents/20123/121286/CSCDA_ESA_Mission-specific+Annex_31_Oct_22.pdf).

## Concept art

`docs/concept/knight.jpg`, the front and back sheet the player knight is
built from (`tools/blender/build_knight.py`), was supplied by the project's
owner for this game. The model is built in code from it; no part of the
image ships in the game.

## The Aether Knight model

`docs/models/aether_knight.glb`, the player knight's model (helm, armor,
cape and its glowing lines, made in parts with no skeleton), was supplied by
the project's owner for use in this game. `tools/blender/build_aether_knight.py`
rigs and decimates it into `assets/characters/aether_knight.glb`; only that
output ships. The build uses
[fast-simplification](https://github.com/pyvista/fast-simplification)
(MIT), a tool dependency that is not shipped with the game.

## Engine

Built with [Godot Engine](https://godotengine.org) 4.6, MIT licence
(© Juan Linietsky, Ariel Manzur and contributors). The web and desktop
exports include the engine under that licence.

## Everything else

Code, shaders, procedural models (the colony's bodies, the luminous plants
and lantern stalks, the glowing realms), sound effects and music: written for
this project. Ash Calder's model, rig and animations are built from scratch by
`tools/blender/build_ash.py`. The trailer's score is synthesized from scratch by
`tools/trailer_music.py` (oscillators and filtered noise, no samples or
recordings), so it belongs to the project like the game's own music. The colony AI can optionally talk to a local Gemma model (see
docs/GEMMA.md); no model weights ship with the game.
