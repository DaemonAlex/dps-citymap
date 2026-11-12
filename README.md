# dps-citymap

A ready-made map of the whole DelPerroSands world, cut into tiles for in-game screens.

## What it is for

In-game screens such as a police computer show a map. The stock map stops at Los Santos and
Blaine County, so Roxwood and Cayo Perico are missing or blank. This resource holds one map
picture that covers all four areas, with postal numbers, so a screen can show the city as
players know it.

## What it does

- Holds 2,327 map tiles (JPG, 256 pixels each) at zoom levels 0 to 5.
- Covers Los Santos, Blaine County, Roxwood and Cayo Perico.
- Serves them to any in-game screen at `https://cfx-nui-dps-citymap/tiles/{z}/{x}/{y}.jpg`.

It has no code. It is a folder of pictures and a manifest.

## On its own, and with other scripts

**On its own.** It does nothing you can see. It only makes the tiles available. Something else
has to ask for them.

**With a paid police computer (wasabi_mdt).** The tiles are cut to the projection the wasabi MDT
map uses: `Transformation(0.02042, 117.3, -0.0208, 172.8)`, 256 pixel tiles, zoom 0 to 5. Point
the MDT map at the tile address above and officers see the full DelPerroSands map with postals.
The MDT only reads the pictures. An MDT update does not change this resource, though you may
have to set the tile address again in the MDT.

**With your own screens.** Any Leaflet map in a NUI page can use the same address and the same
projection.

## Requirements

- None to run it.
- A map screen that can load tiles from a URL, for example wasabi_mdt (paid).

## Install

1. Put the folder in your resources and add `ensure dps-citymap`.
2. In the script that shows the map, set the tile address to
   `https://cfx-nui-dps-citymap/tiles/{z}/{x}/{y}.jpg`.
3. Restart that script.

## Configuration

There are no settings. These are the facts a map screen needs:

| Item | Value |
|---|---|
| Tile address | `https://cfx-nui-dps-citymap/tiles/{z}/{x}/{y}.jpg` |
| Tile size | 256 pixels |
| Zoom levels | 0 to 5 |
| Projection | `Transformation(0.02042, 117.3, -0.0208, 172.8)` |

## Recent changes

- **12 November 2026.** README added.
- **25 October 2026.** First commit, as it runs on DelPerroSands.
- **3 October 2026.** Tiles built.

## Author

Made by [DaemonAlex](https://github.com/DaemonAlex) for DelPerroSands.

The map artwork comes from the BigDaddy postal map textures. Those textures are licensed for
the DelPerroSands server only. If you run another server, get your own licence from BigDaddy
before you use these tiles.

## Other DPS scripts

All of these are made for DelPerroSands and run together on one Qbox server. Each one works on
its own. The ones marked "pairs with" do more when both are running.

| Script | What it does |
|---|---|
| [dps-inventory](https://github.com/DaemonAlex/dps-inventory) | The inventory: ox_inventory with equipment slots, backpacks, armour plates and a self status panel, in the DelPerroSands colours. |
| [dps-medical](https://github.com/DaemonAlex/dps-medical) | Patient records, illness and diagnostic tests. A companion to wasabi_ambulance. Pairs with dps-inventory: symptoms and diagnoses show on the status panel. |
| [dps-insurance](https://github.com/DaemonAlex/dps-insurance) | Ties m-Insurance into the MDT, impound, hospital and medical chart. Pairs with dps-medical. |
| [dps-studio](https://github.com/DaemonAlex/dps-studio) | Build rooms, doors and portals in game from one panel (`/studio`), with owners and managers so staff do not have to support them. |
| [dps-shops](https://github.com/DaemonAlex/dps-shops) | Shop clerks who greet and react to a robbery, then player-owned shops. |
| [dps-fleet](https://github.com/DaemonAlex/dps-fleet) | Vehicle browser and workshop on one panel: extras, liveries and mods for emergency vehicles. |
| [dps-parking](https://github.com/DaemonAlex/dps-parking) | Parking with valet, impound, violations and reserved spots. |
| [dps-vehiclepersistence](https://github.com/DaemonAlex/dps-vehiclepersistence) | Vehicles stay where they were parked. Pairs with dps-parking. |
| [dps-towjob](https://github.com/DaemonAlex/dps-towjob) | Queue-based tow job with jg-mechanic integration. |
| [dps-services](https://github.com/DaemonAlex/dps-services) | Request a tow and follow it live on the lb-phone and lb-tablet. Pairs with dps-towjob. |
| [dps-autoshops](https://github.com/DaemonAlex/dps-autoshops) | Self-service repair shops when no mechanic is on duty. |
| [dps-cityworker](https://github.com/DaemonAlex/dps-cityworker) | City infrastructure job and career. |
| [dps-ainpcs](https://github.com/DaemonAlex/dps-ainpcs) | NPCs you can talk to, with trust, quests and intel. |
| [dps-badpeds](https://github.com/DaemonAlex/dps-badpeds) | Police interaction with NPCs: stops, arrests, intel and jail records. |
| [dps-gangwars](https://github.com/DaemonAlex/dps-gangwars) | Ambient gang NPCs, territory population and war reinforcements. |
| [dps-rotations](https://github.com/DaemonAlex/dps-rotations) | Moves dealers, harvests and other spots on a fixed schedule. |
| [dps-trains](https://github.com/DaemonAlex/dps-trains) | The train system. Pairs with dps-trains-stock, dps-traintools and dps-transitapp. |
| [dps-transitapp](https://github.com/DaemonAlex/dps-transitapp) | Live train arrival boards on the lb-phone. |
| [dps-faceplant](https://github.com/DaemonAlex/dps-faceplant) | City help, reports and staff tools on the lb-phone and lb-tablet. |
| [dps-chat](https://github.com/DaemonAlex/dps-chat) | A command box for voice-only servers. No chat feed. |
| [dps-filmmode](https://github.com/DaemonAlex/dps-filmmode) | One key hides every HUD layer and gives a smooth free camera for recording. |
