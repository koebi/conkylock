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

The conkyrc is configured to display

	BAT: 101 %
	TIME: DD/MM HH:MM

at the moment, and since this works for me, I probably am not going to change
anything. The current colors are a light blue similar to the i3-default-blue
for the BAT/TIME and white for the actual values.

Why this exists
---------------

Lately, there was a bug in i3lock, which made it possible to view notifications
or the i3bar after the screen was locked.
After the fix, someone complained that he used this to view the clock in his
i3bar. A friend of mine then had the idea to use conky, which can draw to a
given window, to display the wanted informations.
