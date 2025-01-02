# linux-mint-themes-snap
A Snap that allows you to use various themes used by Linux Mint in Snap applications.

Unfortunately, you still need to use this command to theme installed Snap apps.
And reuse them when installing new Snap apps.

``` for i in $(snap connections | grep gtk-common-themes:gtk-3-themes | awk '{print $2}'); do sudo snap connect $i linux-mint-themes:gtk-3-themes; done ```

I tried adding the icons used by Linux Mint, but they don't work very well, so I recommend using the Papirus icons:

https://github.com/PapirusDevelopmentTeam/papirus-icon-theme

https://snapcraft.io/icon-theme-papirus

To make it easier for anyone using Snap on Linux Mint, I also added the Snap installation to the script, if it hasn't already been done, as well as the installation of the Snap Store and the Snap version of the Papirus icons.
