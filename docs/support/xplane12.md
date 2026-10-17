---
description: "Set up BeyondATC with X-Plane 12: the BeyondATC plugin, traffic models, what works differently from MSFS, and how to fix common problems."
og_description: "Set up BeyondATC with X-Plane 12: the BeyondATC plugin, traffic models, what works differently from MSFS, and how to fix common problems."
---

# X-Plane 12 (Experimental)

!!! warning "Experimental feature"
    X-Plane 12 support is an **experimental** feature. To use BeyondATC with X-Plane 12 at the moment you require the supporters edition of BeyondATC. X-Plane 12 support will come to all base edition holders for free once it is ready for full release. Please report any bugs via our [bug reporting process](#reporting-a-problem).

BeyondATC works with X-Plane 12 through the **BeyondATC plugin**, which is a small X-Plane plugin that allows BeyondATC to communicate with X-Plane. This page explains what you need, how to install the plugin and traffic models, what works differently from Microsoft Flight Simulator, and how to fix common problems.

---

## Requirements

- **X-Plane 12** on Windows. Version **12.04 or later** is supported
- The **BeyondATC plugin**, which can be installed through the BeyondATC installer (see below)
- **Traffic models** for X-Plane (see [Traffic models](#traffic-models))
- A **flight plan**: SimBrief for IFR flights, and SimBrief or a flight plan file for VFR flights (see [Flight plans](#flight-plans))

---

## Installing the BeyondATC plugin

### With the installer (recommended)

When you run the BeyondATC installer, it looks for your X-Plane 12 installations. If it finds any, it shows an **X-Plane 12 plugin** page which allows you to select which installations should have the BeyondATC plugin.

X-Plane must be closed to install or update the plugin.

!!! info "Your Bluebell models will not be overwritten"
    The installer only writes the plugin's own files. It never changes the `CSL` folder where you keep your Bluebell models.

### Manually

If the installer did not find your X-Plane 12 installation, you can copy the plugin yourself:

1. Close X-Plane.
2. Copy and overwrite the `BeyondATC` folder from the `X-Plane Plugin` folder in your BeyondATC installation directory (by default `C:\BeyondATC\X-Plane Plugin\BeyondATC`) into `X-Plane 12\Resources\plugins\`.
3. Check that the following file exists: `X-Plane 12\Resources\plugins\BeyondATC\win_x64\BeyondATC.xpl`.

### Checking the plugin

Start X-Plane and open **Plugins > BeyondATC**. The first line shows the plugin version, for example **BeyondATC Plugin v1.0.0**. The menu also has:

| Menu item | What it does |
|---|---|
| **Show Traffic Labels** | Shows labels on BeyondATC traffic within 5 NM. This is defaulted to off. |
| **Show Connection Stats** | Opens a small about window with the plugin version, the number of active aircraft, and the data sent and received. |
| **Show Aircraft List** | Allows you to view the BeyondATC traffic that X-Plane is drawing, with callsign, type and phase of flight. |

!!! warning "Cannot see the plugin menu?"
    If **BeyondATC** is not in the Plugins menu, open **Plugins > Plugin Admin** and check that the plugin is installed and enabled. If you cannot see it in Plugin Admin, try running the installer again.

---

## Traffic models

Like MSFS, BeyondATC uses supported models to show our traffic within the simulator. We only support models made and licensed for the simulator used. On X-Plane 12 we support the following models:

| Library | Where to install |
|---|---|
| **Bluebell CSL** | `X-Plane 12\Resources\plugins\BeyondATC\CSL\` |
| **X-CSL** | Install with the X-CSL updater pointed at your X-Plane executable, into `X-Plane 12\Resources\plugins\IVAO_CSL\CSL\` (see below). We're looking at supporting custom locations. |
| **Traffic Global** (Just Flight) | Install as normal, in `X-Plane 12\Aircraft\Traffic Global`. |

To see BeyondATC traffic, you need at least one of them. If you have more than one, you can choose which BeyondATC prefers in **Options > X-Plane Matching Priority**. By default, Traffic Global is matched first, then X-CSL, then Bluebell.

### Bluebell CSL

Download the Bluebell packages from the [Bluebell project](https://github.com/oktal3700/bluebell) and put each `BB_...` package folder directly in `X-Plane 12\Resources\plugins\BeyondATC\CSL\` (create the `CSL` folder if it does not exist). BeyondATC only uses this folder: models in the folders of other plugins, such as LiveTraffic or xPilot, are not used.

!!! warning "The Airbus and Boeing packages may come in parts"
    `BB_Airbus` and `BB_Boeing` are split into parts (`BB_Airbus1`, `BB_Airbus2`, `BB_Boeing1` to `BB_Boeing3`). Each package must be in **one** folder, or the aircraft in parts 2 and 3 are not loaded. That includes many wide-bodies and the A321.

    1. Copy the contents of `BB_Airbus2\BB_Airbus` into `BB_Airbus1\BB_Airbus`.
    2. Copy the contents of `BB_Boeing2\BB_Boeing` and `BB_Boeing3\BB_Boeing` into `BB_Boeing1\BB_Boeing`.
    3. Delete the `BB_Airbus2`, `BB_Boeing2` and `BB_Boeing3` folders.

    To check, open X-Plane's `Log.txt` and look for **BATC: Total CSL models loaded:**. With the full Bluebell set it should say **2027**.

### X-CSL

Install X-CSL with the X-CSL updater as normal: press **Browse** and select your X-Plane executable (`X-Plane.exe`). The updater then installs the models in `X-Plane 12\Resources\plugins\IVAO_CSL\CSL\`.

!!! warning "Do not use Set Custom Path"
    BeyondATC cannot find X-CSL models installed with **Menu > Set Custom Path** in the X-CSL updater. If you have used it, select your X-Plane executable with **Browse** again and update the packages. We are looking into supporting custom locations.

If you want to keep the models on a different drive, install them as above first, then see [Using models from another folder (junctions & symbolic links)](#using-models-from-another-folder-junctions-symbolic-links).

### Traffic Global

Install Traffic Global as normal, then disable the **Traffic Global plugin** (see the note below). If it stays enabled, you will see its own traffic as well as BeyondATC's. BeyondATC cannot see or control traffic injected by other injectors.

!!! note "Disable the Traffic Global plugin"
    For the Just Flight Traffic Global models, you need to disable the Traffic Global plugin itself so that it does not inject its own traffic. BeyondATC still uses the models. There are two ways:

    - **Rename the plugin file (recommended).** Rename `X-Plane 12\Resources\plugins\Traffic Global\win_x64\Traffic Global.xpl` to `Traffic Global.bak`. It then stays disabled, and you can rename it back at any time.
    - **Plugin Admin.** Disable the **Traffic Global** plugin in **Plugins > Plugin Admin**. This has to be done again every time you restart X-Plane.

### Using models from another folder (junctions & symbolic links)

If you already have models in a different location, for example Bluebell models installed in another plugin's folder, or you store models on a different drive, you can make a junction or symbolic link instead. Symbolic links are a part of Windows that let you point (link) one folder to another folder ([Microsoft: Symbolic links](https://learn.microsoft.com/en-us/windows/win32/fileio/symbolic-links)). To set up a symbolic link you can do the following.

1. Close X-Plane.
2. Make sure there is no existing folder that will conflict, for example if you are linking Bluebell models from another place, rename or delete the empty `X-Plane 12\Resources\plugins\BeyondATC\CSL\` folder (if it exists).
3. Open **Command Prompt** (search for `cmd` in the Start menu).
4. Type the command below, **replace drive paths as required**, and press Enter. The first path is the link you want to make, the second path is the folder where the models are already installed.

    For example, say I have my Bluebell CSL models in `D:\My CSL Models`, and I have my X-Plane install in `C:\X-Plane 12\` - I will need to run the following:

    ```
    mklink /J "C:\X-Plane 12\Resources\plugins\BeyondATC\CSL" "D:\My CSL Models"
    ```

    Make sure you put paths in quotation marks (") when they have spaces in them. When the link is created you will see `Junction created for ...`.

5. Start X-Plane. To check it has worked, open X-Plane's `Log.txt` and look for **BATC: Total CSL models loaded:**.

You can do the same for X-CSL. Make the link at the folder the X-CSL updater installed to (by default `X-Plane 12\Resources\plugins\IVAO_CSL\CSL`), pointing to the folder where your X-CSL models are.

!!! note "About links"
    - `mklink /J` makes a **junction**. It does not need administrator rights, and works with any drive in your PC, **but not with network drives**.
    - `mklink /D` makes a **symbolic link**, which also works, including with network drives. It needs a Command Prompt opened with **Run as administrator**.
    - The rules for the models are the same through a link. For example, the Bluebell `BB_Airbus` and `BB_Boeing` packages must still each be in one folder (see above).
    - To remove a link, type `rmdir` and the path of the link in Command Prompt, for example `rmdir "C:\X-Plane 12\Resources\plugins\BeyondATC\CSL"`. This removes only the link, not the models it points to. If you uninstall BeyondATC and choose to remove the Bluebell models, only the link is removed as well.

---

## Setting up X-Plane 12

- **Disable other traffic plugins.** In **Plugins > Plugin Admin**, disable or do not run products such as LiveTraffic, xPilot, X-IvAp/Altitude, swift, the Traffic Global plugin etc. If you run these programs with BeyondATC the plugins will fight for X-Plane's TCAS and/or show their own traffic that BeyondATC cannot see or control.
- **Turn off X-Plane's own ATC.** In **Settings > Sound**, under **Air Traffic Control**, turn off **Enable verbal ATC messages** and **Auto-show ATC message history**.
- **Use real weather.** Historic weather is currently not supported.
- **Set the appropriate time.** Like MSFS, scheduled traffic will be injected following X-Plane's sim time.

---

## Flight plans

- **IFR flights** use your **SimBrief** flight plan.
- **VFR flights** can use **SimBrief** or a **flight plan file**. Select **VFR** on the BeyondATC main menu, choose the file option and select your file. These file types are supported:

| File type | Extension |
|---|---|
| X-Plane Flight Plan | `.fms`, v11 format (X-Plane 12 saves these in `X-Plane 12\Output\FMS plans`) |
| MSFS Flight Plan | `.pln` |
| Little Nav Map Plan | `.lnmpln` |

The flight plan must start and end at an airport. With a flight plan file, BeyondATC reads your aircraft type and tail number, for your callsign, from X-Plane, so your aircraft must have a tail number set. The **MSFS World Map** option is for MSFS only.

---

## Starting a flight

1. Start **X-Plane 12** and load your flight.
2. Start **BeyondATC** and click **Fly**.

BeyondATC will show **Connecting to X-Plane 12...** and then **Connected to X-Plane 12** at the top right. If X-Plane 12 and Microsoft Flight Simulator are both running, you will be asked which simulator you want BeyondATC to use.

!!! info "Pausing is not supported"
    As with MSFS, pausing is not currently supported: BeyondATC's controllers and traffic keep running while X-Plane is paused, so the traffic will have moved on when you unpause. If you need to pause for an extended period, you can exit BeyondATC and start mid-flight at any time.

---

## What's different from MSFS

| Feature | On X-Plane 12 |
|---|---|
| In-sim toolbar | Not available. Use the BeyondATC app. |
| In-sim taxi arrows | In-sim taxi arrows are currently not available. |
| Flight plan import | SimBrief, and for VFR flights a flight plan file (`.fms`, `.pln` or `.lnmpln`). The MSFS world map import is MSFS only. |
| Weather | X-Plane supports live weather only. The MSFS 2024 **Enable Historic Weather** option has no effect. |
| Aircraft with custom datarefs | Some aircraft use their own radio systems and may not follow frequency changes from BeyondATC. If you find BeyondATC cannot read or send frequencies from your X-Plane aircraft, please submit a bug report. |

---

## Known limitations

As an experimental feature, X-Plane 12 support has some known limitations:

- Some older models do not animate their gear, wheels or engines. Where the model supports it, BeyondATC animates flaps, slats, spoilers, reversers, lights and wheels on traffic.
- There is no tire smoke on landing and no engine heat haze for BeyondATC injected traffic.
- Some airports may contain incomplete taxi data. BeyondATC warns you before the flight. You can still use these airports; however, you will be told to taxi at your discretion, and AI traffic will despawn when off the runway.
- After you update your Navigraph data in X-Plane, restart BeyondATC.

---

## Troubleshooting

??? question "Error: Cannot establish a connection with X-Plane"
    BeyondATC could not reach the plugin.

    - Check that X-Plane 12 is running with a flight loaded.
    - Check that **Plugins > BeyondATC** exists in X-Plane. If not, install the plugin (see [Installing the BeyondATC plugin](#installing-the-beyondatc-plugin)) and check **Plugins > Plugin Admin**.
    - Restart X-Plane, then start BeyondATC again.

??? question "Could not connect to a flight simulator"
    BeyondATC did not find a running simulator. Start X-Plane 12 and load your flight **before** you click **Fly** in BeyondATC.

??? question "Your BeyondATC X-Plane plugin is outdated"
    Your version of BeyondATC needs a newer plugin. Close X-Plane, run the BeyondATC installer again with your X-Plane installation checked on the **X-Plane 12 plugin** page, then start X-Plane and BeyondATC again.

??? question "Does BeyondATC support other X-Plane versions?"
    No, BeyondATC supports X-Plane 12 only.

??? question "What operating systems does BeyondATC support?"
    BeyondATC is currently only available on the Windows operating system.

??? question "No traffic models found, traffic will not be displayed"
    BeyondATC did not find any models it can use. Install at least one library (see [Traffic models](#traffic-models)) and restart X-Plane and BeyondATC. For Bluebell, check that the `BB_...` folders are directly in `X-Plane 12\Resources\plugins\BeyondATC\CSL\`.

??? question "X-Plane 12 was not found, so the traffic models could not be checked"
    BeyondATC could not find your X-Plane 12 installation. If you have freshly installed X-Plane 12, start X-Plane at least once before you start BeyondATC.

??? question "X-Plane denied TCAS to BeyondATC"
    Another traffic plugin is holding X-Plane's TCAS. Disable LiveTraffic, xPilot, X-IvAp/Altitude and swift in **Plugins > Plugin Admin**, then restart BeyondATC.

??? question "The Traffic Global plugin is running in X-Plane"
    You see Traffic Global's own traffic as well as BeyondATC's. Disable the Traffic Global plugin: the recommended way is to rename `X-Plane 12\Resources\plugins\Traffic Global\win_x64\Traffic Global.xpl` to `Traffic Global.bak`, so it stays disabled (you can rename it back at any time). Disabling it in **Plugins > Plugin Admin** also works, but has to be done again every time you restart X-Plane. BeyondATC still uses the Traffic Global models. See [Traffic Global](#traffic-global).

??? question "Failed to open the connection to the BeyondATC plugin"
    Another program may be blocking the connection between BeyondATC and the plugin. Close other flight simulation tools, restart your PC, and try again. If it keeps happening, [report a problem](#reporting-a-problem) with your logs.

??? question "Many wide-bodies or A321s are missing"
    If using Bluebell models, your Airbus or Boeing package is probably still split into parts. See [The Airbus and Boeing packages may come in parts](#bluebell-csl).

??? question "Aircraft registration could not be detected from X-Plane"
    You started a VFR flight with a flight plan file, and your aircraft has no tail number set in X-Plane. Use an aircraft with a tail number, or use a SimBrief flight plan instead.

??? question "The MSFS World Map flight plan is only available with MSFS"
    The **MSFS World Map** option of a VFR flight reads the flight plan from MSFS. On X-Plane 12, select a flight plan file or use SimBrief (see [Flight plans](#flight-plans)).

??? question "This X-Plane flight plan uses an old format"
    BeyondATC reads X-Plane flight plans in the v11 `.fms` format, the format that X-Plane 11 and X-Plane 12 save. Older `.fms` formats are not supported. Save the flight plan again from X-Plane 12 or export it from your flight planner in the correct format.

??? question "The installer did not show the X-Plane 12 plugin page"
    The installer did not find an X-Plane 12 installation. Start X-Plane 12 once, close it, and run the installer again, or [install the plugin manually](#manually).

---

## Uninstalling

When you uninstall BeyondATC, it also removes the BeyondATC plugin from your X-Plane 12 installations. If X-Plane is running, you are asked to close it first. You are then asked whether to also remove the Bluebell models in the plugin's `CSL` folder. If you select **No**, they stay on your computer.

---

## Reporting a problem

X-Plane 12 support is experimental, so your reports help us a lot. When you report a problem, include:

- Your BeyondATC log files (see [How to get your log files](bug-reporting.md#how-to-get-your-log-files)).
- X-Plane's `Log.txt`, in your X-Plane 12 folder.

Please report problems in our [Discord](https://discord.gg/beyondatc), following the [bug reporting guide](bug-reporting.md).
