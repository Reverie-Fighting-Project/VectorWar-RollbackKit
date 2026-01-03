### VectorWar RollbackKit

Code changes to the VectorWarUE project to be built using the RollbackKit. This project requires [GGPOUE](https://github.com/koenjicode/GGPOUE).

![screencap](vwscreen.png)

## Setup

1. Install [Unreal Engine 5.7](https://docs.unrealengine.com/en-US/GettingStarted/Installation/index.html), [Visual Studio](https://docs.unrealengine.com/en-US/Programming/Development/VisualStudioSetup/index.html), and any dependencies.
2. Clone the repo with ```git clone --recursive https://github.com/BwdYeti/VectorWarUE.git```, or after downloading run ```git submodule update --init --recursive``` to download the [GGPOUE](https://github.com/koenjicode/GGPOUE) submodule.
3. (optional) Generate project files (Right click VectorWarUE.uproject, ```Generate Visual Studio project files```).
4. Open VectorWarUE.uproject

## Controls

* Arrow keys: Move
* D: Fire
* P: Network Performance Monitor

## Notes

Unreal Engine is not deterministic, which is required for netcode that only sends inputs between players, such as deterministic lockstep (delay based) or rollback. The original VectorWarUE project ran the VectorWar game state, and rendered the game state by matching it with equivalent Unreal Actors. The goal of the RollbackKit is to create a similar workflow that you'd have for working on a proper Unreal Engine project with the added benefit of Rollback.

Currently GGPOUE is only usable with Windows.
