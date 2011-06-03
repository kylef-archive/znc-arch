This is a Archlinux package which contains rc.d scripts for ZNC.

    pacman -U https://github.com/downloads/kylef/znc-arch/znc-system-wide-1.0-1-any.pkg.tar.xz

Once installed you can create a znc config with:

    /etc/rc.d/znc makeconf

And then run ZNC:

    /etc/rc.d/znc start

You can rehash with:

    /etc/rc.d/znc rehash

Adding znc to the DAEMONS (/etc/rc.conf)

    DAEMONS=(... network ... @znc)

When you install this package (znc-system-wide), a user and group named znc will be created. The config for ZNC will be located at `/var/lib/znc`.

Using rc.d scripts with an existing ZNC config
----------------------------------------------

You can edit the contents of the /etc/conf.d/znc file by changing the variables to point to your config and user.
