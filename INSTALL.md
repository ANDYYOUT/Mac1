>(Note: This is meant for the XFCE4 desktop / Xubuntu
>If you don't have it, run "sudo apt install xfce4" or
>"sudo apt install xubuntu-desktop")
>
Hey.

So you downloaded the pack, you actually want to use this.

Maybe you want to prank your friends, or maybe you just want to experience that 1984-style FEEL.

So how do you install it?

Simple.

# The main theme

First off, create the ".fonts", ".themes", and ".icons" in your home folder.
You can use your standard file manager, but I prefer the terminal.
If you do use a terminal, type this in:

"mkdir ~/.themes ~/.icons ~/.fonts"

Otherwise, it's just a quick-and-easy job.

If you don't see it, press Ctrl+H in your file manager (or whatever it's mapped to).

First, move the Chicago font (Chicago.ttf) and the Monaco font (Monaco.ttf) to the .fonts folder.

Copy the icon theme (Mac1Icons) to ~/.icons, and copy the GTK2/XFWM theme to ~/.themes

Now go into "Settings > Appearance", then set the icon theme and GTK theme to "Mac1".

Make sure you also change the fonts

Also in Appearance, go to "Settings" and uncheck "Show icons on buttons" and "Show icons in menus"

Then go into "Settings > Window Manager, and in the "Style" tab, set the theme to "Mac1"
Make sure you change the button layout to look like this

Title alignment : Center

Button Layout : [x][	Title	][#][-]

After that's done with, go into the desktop settings (just right click on the desktop), and switch the style to "None".
then have the color mode set to "Solid Color" and have the actual color be this code:

\#868686

I don't recommend setting it to pure black/white, as that's more obstructing.

And I know the 128k (The original Mac) doesn't use shades of gray, but this is just easier on the eyes.

But if you do want to go the extra mile \(or kilometer), go into the Mac1 Icons, and there should be a file called Tile.png

Just make sure that the desktop setting has it set to "Tiled" before you select it.


# Panel

Now we get to the fun part, the panel.

In case you haven't known by now, Macs have a "global menu", meaning that all options for the program are in the top panel, instead 
of a right-click menu or tabs withing the program.

The easiest way to do this (in any Debian-based distro) is "sudo apt install xfce4-appmenu-plugin"
Just note it won't add it automatically.


There's two ways of setting up the panel items:

## Panel Preferences > Backup and Restore > Import

There should be a Mac1 Panel Config file in the "Mac1-master" folder, or wherever you put it.

## Manual config

So here's the panel config you need to use:

1.) Applications Menu (Uncheck "show icons in menu" and "show button title", set the icon to either the White or Black Apple icon
found in the Mac1 icons folder.

2.) AppMenu / Global Menu (Uncheck "Use bold application name" and "Use Compact mode")

3.) Separator (Transparent + Expanding)

4.) Notification Plugin / Indicator Plugin

(Optional: PulseAudio Plugin)

5.) Separator (Transparent)

6.) Clock, not Orage Clock (Uncheck "Show frame", Line 1 set to "%I:%M %p", Tooltip set to "%A %d %B %Y")

7.) Window Buttons (Button Layout: Icon, uncheck "Show workspace names", check "Show windows from all workspaces"

The only thing left to fiddle with is the panel size.

Uncheck "Don't reserve space on borders", set the row size to 26, number of rows to 1, and the length to 100% (duh).

And set the panel color to pure white while you're at it.

# Miscellaneous Options

If you want you can also edit the Applications Menu... menu... to better suit the look.  Just make sure you add a Log Out/Shutdown
button at the end. :)

If possible, study the layout of an actual Macintosh (There's plenty of pics online, and even some online emulators for it)

If you want the classic outline dragging, then go into "Settings > Window Manager > Advanced" and in "Hide content of windows",
check "When moving" and "When resizing"

Then go into "Settings > Window Manager Tweaks > Compositor" and uncheck "Enable display compositing".  Not only will it allow
full outline dragging, but it also disables shadows, which take away the old school look.



# FAQ

Q: Why did you make this to begin with?

A: Just for fun.  I also wanted to see how it'd acutally work out.


Q: The theme is broken!  The appmenu doesn't look right!

A: In case you haven't read it, this is a -->GTK2<-- theme, which means that GTK3 apps, including the appmenu and other apps (including most GNOME apps), won't
work with this theme.  I'm not going to port it, mostly because I have no idea how to make a GTK3 theme.


Q: Why are there two variants of the Apple icon?

A: `\/(:|)\/`. The black Apple icon can be visible from normal view, but when clicked, it goes completely black. The white Apple 
icon can't be viewed from normal view, but when clicked, it's fully visible. So it really depends on preference.


Q: Why can't you invert the Apple icon on click anyways?

A: Haven't figured it out yet.  Couldn't even find tutorials or forum posts on how to do it, so if you know, just file an issue with the complaint/answer


Q: Are you going to port this to GTK3?

A: Not by a longshot.  Unless I figure out how to make a color variation of something like Numix \(where the colors are actually correct!) or they change it back in GTK5/6, I won't be porting it any time soon.
