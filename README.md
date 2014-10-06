conkylock
=========

little script wrapped around i3lock to display battery status and time on the lockscreen


usage
-----

Put the given conkyrc in ~/.conkyrc and the given conkylock-script in any place
you want.
I use my .i3/config-file to map conkylock to my ThinkVantage-Button using

	bindcode 156 exec ~/.conkylock

Note that you might have to change the i3lockpath to match your personal
settings. Right now, it just starts i3lock as-is.

Why this exists
---------------

Lately, there was a bug in i3lock, which made it possible to view notifications
or the i3bar after the screen was locked.
After the fix, someone complained that he used this to view the clock in his
i3bar. A friend of mine then had the idea to use conky, which can draw to a
given window, to display the wanted informations.
