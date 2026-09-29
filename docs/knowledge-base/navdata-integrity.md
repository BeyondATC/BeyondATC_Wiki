---
hide:
  - navigation
  - toc

og_description: Why BeyondATC warns about a navigation data problem at your airport, and how to clear the simulator's scenery indexes to fix missing or broken procedures.
description: Why BeyondATC warns about a navigation data problem at your airport, and how to clear the simulator's scenery indexes to fix missing or broken procedures.

---

# Navigation data problem warning

!!! warning "Did BeyondATC send you here?"
    If you opened this page from the warning in BeyondATC, please complete the steps in [How to fix it](#how-to-fix-it) before you fly. Until you do, ATC at the affected airport will not work correctly. The steps involve restarting the simulator, so you will need to load your flight again afterwards.

When you load a flight, BeyondATC reads the procedures for your departure and arrival airports (SIDs, STARs and approaches) directly from the simulator. Sometimes the simulator hands over these procedures with the positions of many of their waypoints missing: the waypoint names are there, but their locations are blank.

When that happens, BeyondATC cannot rebuild the published routes, so an approach can end up as little more than a straight line to the runway. The problem is in the data the simulator provides, not in your flight plan, and it has been seen with up-to-date navigation data. It most often appears after an AIRAC cycle update, when MSFS keeps using stale scenery indexes.

BeyondATC checks both airports each time it loads them and shows this warning when it finds the problem. BeyondATC does not stop your flight, but ATC at the affected airport will not behave as expected until the problem is fixed.

!!! info "Help get this fixed in the simulator"
    We have reported this problem to Asobo: [Facilities API returns wrong/corrupt navdata after AIRAC updates](https://devsupport.flightsimulator.com/t/facilities-api-returns-wrong-corrupt-navdata-after-airac-updates/18552). If you've seen this warning, please sign in to the MSFS DevSupport forum and **vote for the report**. The more votes it gets, the more likely it is to be prioritised for a fix.

## What you may notice

- SIDs or STARs missing, or not matching your chart
- Being vectored to the wrong end of the runway
- Being told you've flown through the final approach course, or an unexpected missed approach
- AI traffic divebombing on approach
- AI traffic doing a 180° turn on the runway after landing

---

## How to fix it

For step 1, try **option A** first. Only use **option B** if the problem is still there afterwards.

### Step 1 - Clear the scenery indexes

=== "Option A - Delete the scenery indexes"

    1. Shut down the simulator.
    2. **If you use Navigraph navdata:** reinstall the current AIRAC cycle through the Navigraph Hub.
    3. Open your scenery indexes folder (paste the path into the Windows Explorer address bar) and delete every file ending in `.DAT`:

        | Simulator | Folder |
        |---|---|
        | MSFS 2020 - Microsoft Store / Xbox | `%LOCALAPPDATA%\Packages\Microsoft.FlightSimulator_8wekyb3d8bbwe\LocalCache\SceneryIndexes` |
        | MSFS 2024 - Microsoft Store / Xbox | `%LOCALAPPDATA%\Packages\Microsoft.Limitless_8wekyb3d8bbwe\LocalCache\SceneryIndexes` |
        | MSFS 2024 - Steam | `%APPDATA%\Microsoft Flight Simulator 2024\SceneryIndexes` |

    4. Start the simulator. It rebuilds the indexes, so the first start may take longer than usual.

=== "Option B - Rebuild through the Community folder"

    1. Shut down the simulator.
    2. Rename your Community folder, for example by adding `_backup` to the end of its name.
    3. Start the simulator and wait until you reach the main menu.
    4. Shut the simulator down again.
    5. Rename your Community folder back to its original name.

### Step 2 - Only if you use Navigraph navdata

1. Shut down the simulator.
2. In the Navigraph Hub, remove the Navigraph navdata for your simulator.
3. Start the simulator and wait until you reach the main menu.
4. Shut the simulator down again.
5. In the Navigraph Hub, install the Navigraph navdata for your simulator again.

### Step 3 - Check that it worked

Start the simulator, then BeyondATC, and load your flight again. BeyondATC reads the airport data from the simulator afresh every time a flight is loaded, so if the warning no longer appears, the problem is fixed.

!!! tip "Still seeing the warning?"
    If the warning comes back after following every step, please [report it](../support/bug-reporting.md) and include your `Player.log`. The log records exactly which airport failed the check and why, which helps us pass the problem on to the right people.
