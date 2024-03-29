[xde-theme-blackbirds -- read me first file.  2021-12-08]: #

xde-theme-blackbirds
===============

Package `xde-theme-blackbirds-1.2.4` was released under CCPL:cc-by-nc-nd-3.0
license 2021-12-08.

This is a theme and a set of backgrounds for the _XDE (X Desktop
Environment)_ that provides a set of backgrounds on
an SR-71 Blackbird theme.
This theme uses the Squared-cadet style from the [`xde-styles`][11]
package.

The source for `xde-theme-blackbirds` is hosted on [GitHub][1].


Release
-------

This is the `xde-theme-blackbirds-1.2.4` package, released 2021-12-08.
This release, and the latest version, can be obtained from [GitHub][1],
using a command such as:

    $> git clone https://github.com/bbidulock/xde-theme-blackbirds.git

Please see the [RELEASE][3] and [NEWS][4] files for release notes and
history of user visible changes for the current version, and the
[ChangeLog][5] file for a more detailed history of implementation
changes.  The [TODO][6] file lists features not yet implemented and
other outstanding items.

Please see the [INSTALL][8] file for installation instructions.

When working from `git(1)`, please use this file.  An abbreviated
installation procedure that works for most applications appears below.

This release is published under CCPL:cc-by-nc-nd-3.0 (primarily because
the base styles used to develop these styles were licensed under this
license).
Please see the license in the file [COPYING][10].

Please note that xde-theme-blackbirds is no longer released as
a tarball and is only released as git commits; use:

    $> ./autogen.sh
    $> ./configure --version

to determine the version associated with a given commit in the
checked out working directory.  Note that this is the same version
as executing:

    $> git describe|sed 's,[-_],.,g;s,\.g*,,'

in the checked out working directory.

Note that only HEAD commits are stable: do not attempt to use any
other commit as only HEAD is synchronized with other packages in
the suite.


Quick Start
-----------

The quickest and easiest way to get `xde-theme-blackbirds` up and
running is to run the following commands:

    $> git clone https://github.com/bbidulock/xde-theme-blackbirds.git
    $> cd xde-theme-blackbirds
    $> ./autogen.sh
    $> ./configure
    $> make
    $> make DESTDIR="$pkgdir" install

This will configure, compile and install `xde-theme-blackbirds` the
quickest.  For those who like to spend the extra 15 seconds reading
`./configure --help`, some compile time options can be turned on and off
before the build.

For general information on GNU's `./configure`, see the file
[INSTALL][8].


Prerequisites
-------------

This package needs the [`xde-styles`][11] package to be useful and also
requires the `xde-setbg(1)` program from the [`xde-ctools`][12] package.


Issues
------

Report issues on GitHub [here][2].


Samples
-------

Following are two samples of screenshots of the theme taken under the
[ADWM][13] window manager:

![adwm.jpg](scrot/adwm.jpg "Wallpaper #1")
![adwm_000.jpg](scrot/adwm_000.jpg "Wallpaper #2")

Following are the eight wallpapers included in the theme:

![blackbirds_flats.jpg](images/blackbirds_flats.jpg "Wallpaper #1")
![blackbird_mountains.jpg](images/blackbird_mountains.jpg "Wallpaper #2")
![blackbirds_parked.jpg](images/blackbirds_parked.jpg "Wallpaper #3")
![blackbird_tarmac.jpg](images/blackbird_tarmac.jpg "Wallpaper #4")
![blackbird_refuel.jpg](images/blackbird_refuel.jpg "Wallpaper #5")
![blackbird_beale.jpg](images/blackbird_beale.jpg "Wallpaper #6")
![blackbird_clouds.jpg](images/blackbird_clouds.jpg "Wallpaper #7")
![blackbirds_suits.jpg](images/blackbirds_suits.jpg "Wallpaper #8")

Following are an additional seventeen wallpapers that may be used to
customize the theme:

![blackbird_afterburn.jpg](images/blackbird_afterburn.jpg "Additional Image #1")
![blackbird_climbing.jpg](images/blackbird_climbing.jpg "Additional Image #2")
![blackbird_drone.jpg](images/blackbird_drone.jpg "Additional Image #3")
![blackbird_fields.jpg](images/blackbird_fields.jpg "Additional Image #4")
![blackbird_highalt.jpg](images/blackbird_highalt.jpg "Additional Image #5")
![blackbird_landing.jpg](images/blackbird_landing.jpg "Additional Image #6")
![blackbird_liftoff.jpg](images/blackbird_liftoff.jpg "Additional Image #7")
![blackbird_nose.jpg](images/blackbird_nose.jpg "Additional Image #8")
![blackbird_oversnow.jpg](images/blackbird_oversnow.jpg "Additional Image #9")
![blackbird_peaks.jpg](images/blackbird_peaks.jpg "Additional Image #10")
![blackbird_photos.jpg](images/blackbird_photos.jpg "Additional Image #11")
![blackbird_piggyback.jpg](images/blackbird_piggyback.jpg "Additional Image #12")
![blackbird_pulse.jpg](images/blackbird_pulse.jpg "Additional Image #13")
![blackbird_runway.jpg](images/blackbird_runway.jpg "Additional Image #14")
![blackbirds_mist.jpg](images/blackbirds_mist.jpg "Additional Image #15")
![blackbird_takeoff.jpg](images/blackbird_takeoff.jpg "Additional Image #16")
![blackbird_valley.jpg](images/blackbird_valley.jpg "Additional Image #17")



[1]: https://github.com/bbidulock/xde-theme-blackbirds
[2]: https://github.com/bbidulock/xde-theme-blackbirds/issues
[3]: https://github.com/bbidulock/xde-theme-blackbirds/blob/master/RELEASE
[4]: https://github.com/bbidulock/xde-theme-blackbirds/blob/master/NEWS
[5]: https://github.com/bbidulock/xde-theme-blackbirds/blob/master/ChangeLog
[6]: https://github.com/bbidulock/xde-theme-blackbirds/blob/master/TODO
[7]: https://github.com/bbidulock/xde-theme-blackbirds/blob/master/COMPLIANCE
[8]: https://github.com/bbidulock/xde-theme-blackbirds/blob/master/INSTALL
[9]: https://github.com/bbidulock/xde-theme-blackbirds/blob/master/LICENSE
[10]: https://github.com/bbidulock/xde-theme-blackbirds/blob/master/COPYING
[11]: https://github.com/bbidulock/xde-styles
[12]: https://github.com/bbidulock/xde-ctools
[13]: https://bbidulock.github.io/adwm

[ vim: set ft=markdown sw=4 tw=72 nocin nosi fo+=tcqlorn spell: ]: #
