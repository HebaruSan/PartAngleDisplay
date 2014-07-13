PartAngleDisplay
================

This is a simple KSP plugin that allows you to surface attach parts at accurate angles.

Simply put, the plugin allows you to display a small window in the VAB/SPH that displays the orientation of the currently selected part as pitch, roll and yaw angles and it also allows you to enter increment values for the pitch, roll and yaw and to apply these to the selected part.

It originally used a single hotkey (Alt-P as it doesn't clash with any of the mods I use). If you do not have a part selected then it will show or hide the window. If you do have a part selected then it will apply the angle increments to the part by simply adding the increment values to the displayed Euler angles and re-setting the rotation of the selected part.  This has strange effects caused by the way that Euler angles work.

Version 0.2 introduced a new way use the plugin.  The original Alt-P hotkey still works the same way but it also now overrides the handling of ALT-WASDQE (the standard part rotation controls with ALT held down) in the stock game (they do the same as the unmodified key, rotate by 90 degrees) to instead rotate by whatever angle increment is entered into the respective field in the dialog.  This allows you to set increment values to 1 (or 0.1 or even 0.01) and then have seamless, accurate rotation of parts.

Version 0.2.1 fixes the handling of the standard pitch keys and makes the angle increments they use configurable.  W/S and Shift-W/S no longer go in opposite directions.  The < and > buttons can be used to cycle the angle setting through 120, 90, 72, 60, 45, 30, 15, 10, 5, 1, 0.1 and 0.01 degrees.  The F key also adjusts the "Fine" angle control (F to cycle down, Shift-F to cycle up and Alt-F to reset to 5).

Version 0.2.2 introduces "Part-relative" mode.  This changes the rotation keys to act around the axes of the currently selected part rather than the usual fixed axes.  E.g. if you rotate a Mk 1 plane cockpit to an odd angle and then switch to "Part-relative" and roll using Q and E the part will roll around its own axis.

It is getting "nicer" though the non-intuitive behaviour of Euler angles is a bit confusing.  I am releasing it as is just in case anyone else finds it useful or wants to develop it further. There are various issues with it (e.g. the editable fields behave quite strange) but it works for what I designed it for (setting the pitch angle of radially attached girders to 2 decimal places).

Change Log
==========
    13/07/2014 16:37 GMT   Implemented "Part-relative" mode that changes all part rotation axes to be relative to the selected part
                           Updated version to 0.2.2.0

    13/07/2014 12:29 GMT   Now totally overrides part rotation hotkeys
                           Allows changing of the default and fine rotation increments
                           Updated version to 0.2.1.0

    10/07/2014 21:52 GMT   Now uses configured key bindings for part rotation rather than hardwired WASDQE
                           Updated version to 0.2.0.2

    10/07/2014 20:53 GMT   Fixed roll and yaw rotation axes in SPH
                           Updated version to 0.2.0.1
                           Fixed version in title bar

    10/07/2014 12:12 GMT   Added handling of ALT-WASDQE to rotate by the entered amounts in the respective axes
                           Updated version to 0.2.0.0

    28/05/2014 09:48 GMT   Added buttons to zero the increment fields
                           Rearranged window to avoid things moving when entering values
                           First release version 0.1.0.1
    
    23/05/2014 14:06 GMT   Fixed editable fields to work better
    
    20/05/2014 23:17 GMT   Removed some unused code and logging
    
    20/05/2014 15:52 GMT   First release

The code is released under the MIT license (see PartAngleDisplay/EditorWindow.cs).
