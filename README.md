This script allows you to change focus based on the relative orientation of windows on the desktop.

![img](https://github.com/rzwisler/focus/blob/master/demo.gif)

# Usage

focus [up|down|left|right]

I use this script via vi-style movement keys in Openbox.  Here are the relevant lines from my ~/.config/openbox/rc.xml:

    <keybind key="W-h">
      <action name="Execute">
        <command>/home/rzwisler/bin/focus left</command>
      </action>
    </keybind>
    <keybind key="W-j">
      <action name="Execute">
        <command>/home/rzwisler/bin/focus down</command>
      </action>
    </keybind>
    <keybind key="W-k">
      <action name="Execute">
        <command>/home/rzwisler/bin/focus up</command>
      </action>
    </keybind>
    <keybind key="W-l">
      <action name="Execute">
        <command>/home/rzwisler/bin/focus right</command>
      </action>
    </keybind>

If you are not running Openbox, you can probably get the same results via programs like **sxhkd** or **xbindkeys**.

# Dependencies

This script requires that you have **xprop** and **wmctrl** installed on your system.  Both are standard utilities that should be easily available via your favorite package manager.
