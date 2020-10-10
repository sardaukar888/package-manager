
# Peeyem

Peeyem is a simple package manager for Microsoft Flight Simulator. It allows you to view all the official and community packages available on your system. Community packages can be enabled or disabled between game sessions to minimize the game's memory foot print.

It works by creating soft links or junctions to the enabled packages. No directories or files are moved when enabling or disabling packages.

## Requirements

.NET Core 3.1 is required to run the application. You can download it [here](https://dotnet.microsoft.com/download/dotnet-core/current/runtime).

## Change Log

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
* Fixed: Crash When an enabled warehouse package was renamed outside the application. (Reported by [influous@FlightSim.to](https://flightsim.to/profile/influous))


v0.2.0, *"Trying to think like an end user"*, 2020-10-04

* New: Introduced and implemented the Package Warehouse concept to replace the Disabled Community Packages directory.
* New: The package thumbnail can be shown in the list.
* New: The business information about a package can be displayed.
* Changed: Renamed the ``Name`` column to ``Location``. It will now display the relative location of the package in the Package Warehouse or the Community packages directory.
* Improved: Various user interface improvements.

v0.1.0, *"Scratchin' the itch"*, 2020-10-01

* Initial release

## Acknowledgements

* Various icons from [Online Web Fonts](https://www.onlinewebfonts.com/).
