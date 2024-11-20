# dotnet-nuget-gc

This `dotnet` extension is designed to clean-up the NuGet cache. It's a
(hopefully) temporary workaround for the [missing cache-expiration
policy][nuget-issue]. 

Code written by [@dotmorten] as outlined in [his
comment][code-origin].

Original github project by [@terrajobst].

Prune code by [@StirlingLabs].

[@dotmorten]: https://github.com/dotMorten
[@terrajobst]: https://github.com/terrajobst
[@StirlingLabs]: https://github.com/StirlingLabs
[nuget-issue]: https://github.com/NuGet/Home/issues/4980
[code-origin]: https://github.com/NuGet/Home/issues/4980#issuecomment-432512640

## Installation

    $ BuildAndInstall-win.ps1

## Usage

    usage: dotnet nuget-gc [options]

    Options:
      -f, --force                Performs the actual clean-up. Default is to do a
                                 dry-run and report the clean-up that would be
                                 done.
      -m, --min-days=VALUE       Number of days a package must not be used in order
                                 to be purged from the cache. Defaults to 90.
      -p, --prune                prune older versions of packages regardless of age
      -?, -h, --help             show this message and exit

