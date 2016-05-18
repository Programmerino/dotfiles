i3 configuration for Ubuntu 16.04
=================================

1. Install i3 and packages:

    ```bash
    # echo "deb http://debian.sur5r.net/i3/ $(lsb_release -c -s) universe" >> /etc/apt/sources.list
    # apt update
    # apt --allow-unauthenticated install sur5r-keyring
    # apt update
    # apt install i3
    # apt install lm-sensors feh vim-gtk unzip lxappearance rofi compton i3blocks gxkb xfce4-volumed pasystray arandr unity-tweak-tool fonts-hack-ttf
    ```

2. Disable IBus:

    Run unity-control-center and go to Personal -> Language Support -> Keyboard input method system: none

3. Install fonts:

    ```bash
    $ wget https://github.com/FortAwesome/Font-Awesome/archive/v4.6.2.zip
    $ unzip v4.6.2.zip
    $ mkdir ~/.fonts
    $ cp Font-Awesome-4.6.2/fonts/fontawesome-webfont.ttf ~/.fonts/
    $ wget https://github.com/supermarin/YosemiteSanFranciscoFont/archive/master.zip
    $ unzip master.zip
    $ cp YosemiteSanFranciscoFont-master/*.ttf ~/.fonts/
    $ sudo fc-cache -f -v
    ```

4. Install Arc Darker theme:

    [Arc Chrome theme]

    [Arc Darker Firefox theme]

    [Arc Darker GTK]:

    ```bash
    $ sudo sh -c "echo 'deb http://download.opensuse.org/repositories/home:/Horst3180/xUbuntu_16.04/ /' >> /etc/apt/sources.list.d/arc-theme.list"
    $ sudo apt-get update
    $ sudo apt-get install arc-theme
    $ wget http://download.opensuse.org/repositories/home:Horst3180/xUbuntu_16.04/Release.key
    $ sudo apt-key add - < Release.key
    ```

5. Install [MOKA ICON THEME]:

    ```bash
    $ sudo add-apt-repository ppa:moka/daily
    $ sudo apt-get update
    $ sudo apt-get install moka-icon-theme
    ```

6. Apply theme and other

    Run lxappearance, unity-tweak-tool, gnome-terminal and change themes, fonts, icons.

    LXAppearance:
    ![LXAppearance](https://i.gyazo.com/cb09d9522e8ad794a4b5da4ae8b4a5d3.png)

    Unity-tweak-tool:
    ![Unity-tweak-tool-1](https://i.gyazo.com/fb548639d28250f4c62483e00e888f59.png)
    ![Unity-tweak-tool-2](https://i.gyazo.com/08de9d2438351bb4817966138daf96ef.png)
    ![Unity-tweak-tool-3](https://i.gyazo.com/ee62e20a71194956e3b882b47ba19a56.png)

    Gnome-terminal:
    ![Gnome-terminal](https://i.gyazo.com/189a11871895417a1ef63090032ed9ee.png)

7. Disable start nautilus wallpaper

    ```bash
    gsettings set org.gnome.desktop.background show-desktop-icons false
    gsettings set org.gnome.settings-daemon.plugins.background active false
    ```

8. Copy files (.config/i3/config, etc)

9. Log out and select i3 desktop environment on LightDM menu and log in. After log in generate first i3 configuration.

## Screenshots

![Screenshot1](https://i.gyazo.com/589f14bb2af5dec1a14745050a27391f.png)

![Screenshot2](https://i.gyazo.com/ffbfa10a41c67ace1ee2a7b04b8c6117.png)

![Screenshot3](https://i.gyazo.com/0a63063af0edc799d6be18daab3674a0.png)

![Screenshot4](https://i.gyazo.com/f274d7c33030a20020a05fc52ebb8041.png)

### Useful links and programs:
xprop - property displayer for X

arandr - ARandR is designed to provide a simple visual front end for XRandR.
         Relative monitor positions are shown graphically and can be changed in a drag-and-drop way.

LXAppearance - theme switcher.

Unity Tweak Tool - is a settings manager for the Unity desktop.

[Font Awesome cheatsheet]

[Font Awesome]

[YosemiteSanFranciscoFont]

[Arc Chrome theme]:https://chrome.google.com/webstore/detail/arc-chrome-theme/oedilkkjhpfhjpbgkloomkpjmficnona
[Arc Darker Firefox theme]:https://github.com/horst3180/arc-firefox-theme/releases
[Arc Darker GTK]:https://github.com/horst3180/Arc-theme
[MOKA ICON THEME]:https://snwh.org/moka/download
[Font Awesome cheatsheet]:https://fortawesome.github.io/Font-Awesome/cheatsheet/
[Font Awesome]:https://github.com/FortAwesome/Font-Awesome/releases
[YosemiteSanFranciscoFont]:"https://github.com/supermarin/YosemiteSanFranciscoFont
