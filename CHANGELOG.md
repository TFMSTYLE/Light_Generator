# Changelog

## 1.2.8

- Updates now come from one place. Installed from the Blender store or from the TFMSTYLE repository, Blender updates this addon itself and the Update button here stays hidden. Installed from a zip, it still updates itself from Relay

## 1.2.7

- Generate Lights and Delete Lights now have their own undo step, so Ctrl+Z takes back only that action. Saving a preset no longer fails on a damaged preset file

## 1.2.6

- Added update checks: when a new version is published on Relay, an Update button appears in this panel. Nothing goes online when Allow Online Access is off, and Blender store installs keep updating through the store

## 1.2.5

The source code is now in this repository, with the license it has always been released under.

- Added the GPL 3.0 license text and a copyright notice
- Set the extension id back to light_generator, the one used on the Blender store
- The package now lists exactly which files it holds
- Restored the store name and tags

## 1.2.4

Packaged after the last store release. What changed was not recorded.

## 1.2.0

Released on the Blender store on 2025-10-29.

- UI styling Changes
- Context aware Editing, create multiple generators and edit them independently
- Lights are now created in an empty object for better functions
- New "Select All Lights" Button to select all lights for better visibility
- Added a delete preset button in the preset tab

## 1.0.2

Released on the Blender store on 2025-10-22.

- Added Tags

## 1.0.1

Released on the Blender store on 2025-10-05.

Changed preset file storage to use Blender’s bpy.utils.extension_path_user for proper write access.

## 1.0.0

Released on the Blender store on 2025-10-03.

First version release.
