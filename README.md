
# package-manager

Peeyem is a simple package manager for Microsoft Flight Simulator. It allows you to view all the official and community packages available on your system. Community packages can be enabled or disabled between game sessions to minimize the game's memory foot print.

It works by creating soft links or junctions to the enabled packages. No directories or files are moved when enabling or disabling packages.

## Requirements

.NET Core 3.1 is required to run the application. You can download it [here](https://dotnet.microsoft.com/download/dotnet-core/current/runtime).

## Changelog

*v0.2.0, "Trying to think like an end user"*, 2020-10-04

* New: Introduced and implemented the Package Warehouse concept to replace the Disabled Community Packages directory.
* New: The package thumbnail can be shown in the list.
* New: The business information about a package can be displayed.
* Changed: Renamed the ``Name`` column to ``Location``. It will now display the relative location of the package in the Package Warehouse or the Community packages directory.
* Improved: Various user interface improvements.

*v0.1.0, "Scratchin' the itch"*, 2020-10-01
* Initial release