# linux-mint-themes-snap
A Snap that allows you to use various themes used by Linux Mint in Snap applications.

<a href="https://snapcraft.io/linux-mint-themes">
    <img alt="Get it from the Snap Store" src=https://snapcraft.io/en/dark/install.svg />
  </a>

Unfortunately, you still need to use this command to theme installed Snap apps.
And reuse them when installing new Snap apps.

``` for i in $(snap connections | grep gtk-common-themes:gtk-3-themes | awk '{print $2}'); do sudo snap connect $i linux-mint-themes:gtk-3-themes; done && for i in $(snap connections | grep gtk-common-themes:icon-themes | awk '{print $2}'); do sudo snap connect $i linux-mint-themes:icon-themes; done ```

I tried adding the icons used by Linux Mint, but they don't work very well, so I recommend using the Papirus icons:

https://github.com/PapirusDevelopmentTeam/papirus-icon-theme

https://snapcraft.io/icon-theme-papirus
