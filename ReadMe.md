
# Peeyem

Peeyem is a simple to use package manager for Microsoft Flight Simulator. It allows you to view all the official and community packages available on your system. Community packages can be enabled or disabled between game sessions to minimize the game's memory foot print.

It works by creating soft links or junctions to the enabled packages. No directories or files are moved when enabling or disabling packages.

## Requirements

.NET Core 3.1 is required to run the application. You can download it [here](https://dotnet.microsoft.com/download/dotnet-core/current/runtime).

## Change Log

v0.6.0, *"Flying a plane is no different than riding a bicycle, just a lot harder to put baseball cards in the spokes."*, 2020-12-06

* Added: "Enable Selected" and "Disable Selected" menu items to the package context menu.
* Added: The set of enabled packages can be saved to and loaded from a file.
* Added: The waypoints of the flight plan of a mission package are displayed on a map.
* Improved: Points of Interests are displayed in the Objects list of the package details panel.
* Improved: Peeyem tries extra hard to determine the real package type of packages of types Core and Unknown.
* Improved: Installing packages with the option "Required files only" takes into account packages with an invalid layout.json file.
* Bug Fix: Failed to correctly read a small category of directory names containing non-ANSI characters.
* Bug Fix: The "Select All from" context menu item did not allow you to select all packages in Official, Community or Warehouse package directory.
* Known Problem: On one configuration Peeyem is be unable to recognize the junctions it creates resulting in an inconsistent view of the Community directory. Thanks to [fredm@FlightSim.to](https://flightsim.to/profile/fredm) for helping me to find the cause of this issue but so far no success.

v0.5.0, *"I feel the need... the need for speed."*, 2020-11-02

* Added: The package detail panel has been moved to the right side of the window to be able to show more information about a package.
  * The airports of a scenery package are shown on a map.
  * The scenery objects of a scenery package are shown on a map.
  * The aircraft configurations are shown with more detail.
  * The package detail panel can be enabled or disabled in the View / Details menu.
* Added: An option to delete the content cache file when you enable or disable a package. You can enable the option in the Environment category of the Options dialog.
* Improved: Various little performance improvements to better cope with large package libraries.
    * Improved: Reading aircraft configurations.
    * Improved: The airports and SimObjects of a scenery package are read on demand and in the background. This should reduce the performance hit when working with large package collections.
* Bug Fix: Changed the value used to show the name of the liveries.

v0.4.1, *"Software testers succeed where others fail."*, 2020-10-22

* Added: "Select All from" sub menu to package context menu to select all packages in the same location or higher as the current selected package. It's more difficult to explain than to use.
* Improved: Various performance optimizations.
  * The thumbnail will no longer be read if you set the thumbnail scale factor to 0.
  * Package analysis has been optimized.
* Improved: Various little user interface tweaks.
  * The package details panel displays the number of airports in a scenery package. The airport list is ordered by ICAO code.
  * You can install package archives in directories by dropping the directory on the package list or the installer dialog.
* Bug Fix: Failed to detect all airports in packages. "Official/fs-base" contains more than 10,000 airports.
* Bug Fix: Packages without a layout.json file caused a crash to desktop.`

v0.4.0, *"The design is perfect, the only flaw is that we have to rely on you to fly it."*, 2020-10-19

* Added: Install and uninstall packages from downloaded archives using Peeyem.
* Added: Drag & Drop support. Drop an archive containing one or more packages on the package list or the installer dialog to install it.
* Added: An aircraft package shows the liveries it contains in the details panel.
* Added: Menu item in the package context menu to copy the liveries of an aircraft package to the clipboard.
* Added: A scenery package shows the airports it contains in the details panel.
* Added: Menu item in the package context menu to copy the airports of a scenery package to the clipboard.
* Added: Peeyem can check if a new version has been released at startup or on demand. The default behavior can be changed in the Options dialog.
* Changed: Folded "Enable / Selected" and "Enable / All" into one "Enable" menu item.
* Changed: Folded "Disable / Selected" and "Disable / All" into one "Disable" menu item.
* Improved: Various little user interface tweaks.
* Bug Fix: The path of the Official Packages directory was not always saved to the settings if it was different from the detected path.
* Bug Fix: Some keyboard shortcuts were broken.

v0.3.0, *"I don't know, I'm making this up as I go."*, 2020-10-10

* Added: All selected packages can be enabled or disabled simultaneously.
* Added: An icon to indicate of something is wrong with a package. The error message is shown in the tool tip of the icon and in the status bar when the package has the focus.
* Added: An icon to indicate the type of the package.
* Added: A display name of the package. In a future version I plan to make the display name updatable by the user.
* Added: The release notes of a package.
* Improved: Various user interface improvements
  * The packages can be sorted by clicking on the column header corresponding to the property.
  * Added a detail panel to show extended details (such as the thumbnail and the release notes) about a package.
  * Added a context menu to the column headers to hide or to reveal individual columns.
  * Added a context menu to the rows with row specific commands.
  * Added a menu to determine which package type are shown.
  * Added a default thumbnail if the package does not provide one.
  * Added a context menu item to a package row to copy the package location to the clipboard.
  * Added a context menu item to a package row to open the package location in Explorer.
  * The width of the columns is remembered.
  * The size of the thumbnail can be set in the Options dialog.
* Improved: You can select the location of the Official packages because its detection algorithm is not full-proof.
* Improved: Internal changes
  * Simplified package reading code.
  * Made reading Community packages more robust. Some packages contain errors in the data or the structure.
  * The logging and error checking has been expanded (but it will never be enough...)
* Fixed: Crash when an enabled warehouse package was renamed outside the application. (Reported by [influous@FlightSim.to](https://flightsim.to/profile/influous))

v0.2.0, *"Trying to think like an end user"*, 2020-10-04

* New: Introduced and implemented the Package Warehouse concept to replace the Disabled Community Packages directory.
* New: The package thumbnail can be shown in the list.
* New: The business information about a package can be displayed.
* Changed: Renamed the ``Name`` column to ``Location``. It will now display the relative location of the package in the Package Warehouse or the Community packages directory.
* Improved: Various user interface improvements.

v0.1.0, *"Scratchin' the itch"*, 2020-10-01

* Initial release

## Acknowledgements / Credits

* Various icons from [Online Web Fonts](https://www.onlinewebfonts.com/).
* Pin icon from Vista Map Markers demo icons [Icons Land]( http://www.icons-land.com/).
* [7-Zip](https://www.7-zip.org/), Copyright (C) 1999-2020 Igor Pavlov.
